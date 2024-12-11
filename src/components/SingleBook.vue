<template>
    <div class="book-details">
        <div class="img-container">
            <img class="book-img" :src="book.image" />
        </div>
        <h2 class="book title">{{book.title}}</h2>
        <p class="book summary">{{book.summary}}</p>
        <p class="book author"> - {{book.author}}</p>
        <div class="tags">
            <p class="book genre">{{book.genre}}</p>
            <p class="book publication_date">{{book.publication_date}}</p>
            <p class="book rating_review">{{book.rating_review}}</p>
        </div>

        <!-- <p class="book suggestions">{{book.related_book_suggestions_images}}</p> -->
    </div>
</template>

<script>
    export default{
        name: 'SingleBook',
        props:{
            book: Object
        }
    }
</script>

<style scoped>
    .book-details{
        display: grid;
        grid-template-columns: 1fr;
        grid-template-rows: 1fr 0.1fr auto .1fr .1fr;
        padding: 20px;
        background-color: white;
        line-height: 1.5rem;
        border-radius: 8px;
        margin-bottom: 1rem;
        /* border: solid #3F51B5; */
        background-color: #70b0ba;
        
    }
    .title {
        text-align: center;
        margin: 0.5rem 0;
        text-transform: uppercase;
        color: rgb(231, 62, 102);
        min-height: 3rem;
        overflow:auto;
        grid-area: auto;
    }
    .author {
        text-align: right;
        font-size: 0.8rem;
        color: #223630;
        font-weight: bold;
    }
    .summary{
        font-size: 0.85rem;
        text-align: justify;
        margin: 0.5rem 0;
        min-height: 100px;
    }
    .img-container{
        width: 100%;
        text-align: center;
    }
    .img-container img{
        width: 100%;
        height:500px;
    object-fit:cover;
    border-radius: 8px;
    border: 2px solid #000;
    }
    .tags {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        grid-gap: 0.5rem;
        justify-content: center;
        margin: 0.5rem 0;
    
    
    }

    .genre, .publication_date, .rating_review{
        color: #000;
        background-color: #FFF;
        padding: 5px 10px;
        border-radius: 5px;
        font-size: 0.8rem;
        letter-spacing: 1px;
        font-weight: bold;
        text-align: center;
        max-height: 35px;
        overflow: auto;

    }

    @media screen and (max-width: 1200px) {
        .book-details {
            padding: 15px;

        }
        .title {
            font-size: 1.5rem;
        }
        .author {
            font-size: 0.7rem;
        }
        .summary {
            font-size: 0.8rem;
        }
        .tags {
            font-size: 0.8rem;
        }
        .genre, .publication_date, .rating_review{
            padding: 3px 5px;
            font-size: 0.75em;
        }

        
    }
</style>