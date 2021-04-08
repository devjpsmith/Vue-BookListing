<template>
    <form action="#" class="" method="post">
        <input type="text" name="title" value="" placeholder="Book Title" v-model="bookTitle">
        <input type="text" name="author" value="" placeholder="Book Author" v-model="bookAuthor">
        <button type="submit" name="button" @onsubmit.prevent="bookSubmit(bookTitle, bookAuthor)">Add Book</button>
    </form>
</template>

<script>
export default {
    name: 'BookForm',
    data() {
        return {
            bookTitle: '',
            bookAuthor: ''
        };
    },
    props: [
        'books'
    ],
    methods: {
        bookSubmit: function (bookTitle, bookAuthor) {
            this.$emit('addBook', bookTitle, bookAuthor);
        }
    }
}
</script>

<style>

</style>