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
        <v-form name="contact" method="post" netlify>
      <v-text-field
        v-show="false"
        v-model="title"
        name="form-name"
      />
      <v-row>
        <v-col cols="12">
          <v-text-field
            v-model="name"
            label="name"
            name="name"
            autofocus
          />
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12">
          <v-text-field
            v-model="email"
            label="E-mail"
            name="email"
          />
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12">
          <v-textarea
            v-model="contents"
            label="message"
            name="message"
          />
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <v-btn
            :disabled="isEmpty"
            type="submit"
          >
            submit
          </v-btn>
        </v-col>
      </v-row>
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