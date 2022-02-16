<template>
    <v-row
    align="center"
    justify="center"
    >
        <v-col
        align="center"
        cols="12"
        sm="6"
        >
        <div
        class="pa-3"
        >
        <h2
        style="text-decoration: underline;"
        >
            Contact
        </h2>
    </div>

        <div
        class="pa-3 text-body-1"
        >
        お仕事のご依頼・ご相談からお茶会のお誘いまでなんでもお気軽にご連絡ください。
        順次なるべく早くお返事致します。
    </div>

<v-container>
    <validation-observer
    ref="observer"
    v-slot= "{ invalid }"
    >
    <form
    method="POST"
    name="contact"
    data-netlify="true"
    data-netlify-honeypod="bot-field"
    @submit.prevent="submit"
    >

    <input type="hidden" value="contact" name="form-name" />
    <div
    v-show="false"
    >
        <input v-model="botField" type="text" name="bot-field" />
    </div>

<validation-provider
v-slot="{errors}"
rules="required"
name="お名前"
>
        <v-text-field
        v-model="name"
        label="お名前"
        :error-messages="errors"
        >   
        </v-text-field>
        </validation-provider>

        <validation-provider
        v-slot="{ errors }"
        rules="required|email"
        name="メールアドレス"
        >
                <v-text-field
        v-model="email"
        label="メールアドレス"
        :error-messages="errors"
        >   
        </v-text-field>
</validation-provider>

<validation-provider
v-slot="{ errors }"
name="お問合せ内容"
rules="required"
>
        <v-textarea
        v-model="contents"
        :error-messages="errors"
        label="内容"
        >
        </v-textarea>
</validation-provider>

        <v-btn
        :disabled="invalid"
        type="submit"
        width="100%"
        color="primary"
        class="mt-5"
        style=
        "
        height: 50px;
        border-radius: 30px;
        "
        @click="clear"
        >
            送信
        </v-btn>
    </form>
</validation-observer>

</v-container>

        </v-col>
    </v-row>
</template>

<script>
export default {
    data() {
        return {
            name: "",
            email: "",
            contents: ""
        }
    },
    methods: {
        clear() {
            this.name=""
            this.email=""
            this.contents=""
            this.$refs.observer.reset()
        }
    }
}
</script>