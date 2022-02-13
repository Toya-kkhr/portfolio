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
        class="pa-3"
        >
              <p>
        texttexttexttexttext
        texttexttexttexttext
        texttexttexttexttext
        texttexttexttexttext
        texttexttexttexttext
        texttexttexttexttext
      </p>
    </div>

<v-container>
    <v-form>
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
        style=
        "
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
            name: "",
            email: "",
            contents: ""
        }
    }
}
</script>