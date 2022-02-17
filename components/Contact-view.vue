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
    v-slot="{ invalid }"
    >
        <v-form 
        name="contact"
        method="post"
        data-netlify-honeypot="botfield"
        netlify
        >

      <v-text-field
        v-show="false"
        v-model="title"
        name="form-name"
      />

    <validation-provider
    v-slot="{errors}"
    name="お名前"
    rules="required"
    >
          <v-text-field
            v-model="name"
            label="name"
            name="name"
            :error-messages="errors"
            autofocus
          />
    </validation-provider>

    <validation-provider
        v-slot="{errors}"
        name="メールアドレス"
        rules="required"
    >
          <v-text-field
            v-model="email"
            label="E-mail"
            name="email"
            :error-messages="errors"
          />
    </validation-provider>

        <validation-provider
            v-slot="{errors}"
            name="メッセージ"
            rules="required"
        >
          <v-textarea
            v-model="contents"
            label="message"
            name="message"
            :error-messages="errors"
          />
        </validation-provider>

            <v-text-field
          v-show="false"
          v-model="botfield"
          >
          </v-text-field>
          <v-btn
            :disabled="invalid"
            type="submit"
          >
            送信
          </v-btn>
    </v-form>
    </validation-observer>
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
            message: "",
            botfield: ""
        }
    },
    methods: {
        submit() {
            
        }
    }
}
</script>