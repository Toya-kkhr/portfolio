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
        その日のうちにお返事致します。
    </div>

<v-container>
    <validation-observer
    ref="observer"
    v-slot="{ invalid }"
    >
      <v-text-field
      v-show="false"
        v-model="contact"
        name="form-name"
      />

    <validation-provider
    v-slot="{errors}"
    name="お名前"
    rules="required"
    >
          <v-text-field
            v-model="name"
            type="text"
            label="name"
            name="name"
            :error-messages="errors"
          />
    </validation-provider>

    <validation-provider
        v-slot="{errors}"
        name="メールアドレス"
        rules="required|email"
    >
          <v-text-field
            v-model="email"
            type="email"
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
            v-model="message"
            label="message"
            name="message"
            :error-messages="errors"
          />
        </validation-provider>

            <v-text-field
          v-show="false"
          v-model="botfield"
          name="bot-field"
          >
          </v-text-field>

          <div
          class="pa-4"
          >
          <v-btn
            :disabled="invalid"
            type="submit"
            width="100%"
            height="50px"
            class="rounded-pill"
            color="primary"
          >
            送信
          </v-btn>
          </div>
    </validation-observer>
</v-container>


              <form
    name="contact"
    method="post"
    data-netlify-honeypot="bot-field"
    netlify
    action="/success"
    >
    <input type="hidden" name="form-name" value="contact" />
    <input type="text" name="name" />
    <input type="email" name="email" />
    <textarea type="text" name="message" />
    <input type="text" name="bot-field" />
    <button type="submit">button</button>
    </form>
        </v-col>
    </v-row>

    
</template>

<script>
export default {
  name: "ContactPage",
    data() {
        return {
            contact: "contact",
            name: "",
            email: "",
            message: "",
            botfield: ""
        }
    },
    methods: {
        submit() {
            const params = new URLSearchParams()
            params.append('form-name', 'contact')
            params.append('name', this.name)
            params.append('email', this.email)
            params.append('message', this.message)

            if(this.botfield) {
              params.append('bot-field', this.botfield)
            }
            this.$axios
            .$post('', params)
            .then()(() => {
              print("success")
            })
            .catch( err => {
              print("error", err)
            })
  
        }
    }
}
</script>