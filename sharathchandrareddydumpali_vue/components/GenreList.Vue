<!-- <template>
    <div class="genre-books">
        <h1 class="genre-title">{{ genre }} Books</h1>
        <div class="books-list">
            <div v-for="book in filteredBooks" :key="book.title"> 
                <SingleBook :book="book" />
            </div>
        </div>
    </div>
</template>

<script>
import SingleBook from './SingleBook.vue';

export default {
    name: 'GenreBooks',
    props: {
        books: {
            type: Array,
            required: true
        },
        genre: {
            type: String,
            required: true
        }
    },
    components: {
        SingleBook
    },
    computed: {
        filteredBooks() {
            return this.books.filter(book => book.genre.toLowerCase() === this.genre.toLowerCase());
        }
    }
};
</script>

<style scoped>
.genre-books {
    width: 100%;
    margin: auto;
    padding: 20px;
}

.genre-title {
    text-align: center;
    font-size: 2rem;
    color: #3f51b5;
    margin-bottom: 20px;
    text-transform: capitalize;
}

.books-list {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
    padding: 0 40px;
    width: 90%;
    margin: auto;
}

</style> -->
