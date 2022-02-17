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
    <v-form
    ref="form"
    name="contact"
    method="POST"
    netlify-honey-pod="bot-field"
    netlify
    >
    <v-text-field v-model="title" type="hidden" name="form-name" />

        <v-text-field v-show="false" name="bot-field" />

        <v-text-field
        v-model="name"
        label="お名前"
        required
        >   
        </v-text-field>

        <v-text-field
        v-model="email"
        label="メールアドレス"
        required
        >   
        </v-text-field>

        <v-textarea
        v-model="contents"
        label="内容"
        required
        >
        </v-textarea>

        <v-btn
        type="submit"
        width="100%"
        color="primary"
        class="mt-5"
        style=
        "
        height: 50px;
        border-radius: 30px;
        "
        >
            送信
        </v-btn>
    </v-form>
</v-container>
        </v-col>
    </v-row>
</template>

<script>
export default {
    data() {
        return {
            title: "contact",
            name: "",
            email: "",
            contents: "",
        }
    },
    methods: {
        submit() {
            
        }
    }
}
</script>