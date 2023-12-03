const url = "https://api.dictionaryapi.dev/api/v2/entries/en/";
const result = document.getElementById("result");
const btn = document.getElementById("search-btn");


async function dictionaryFn(word)
{
    const res=await fetch(`https://api.dictionaryapi.dev/api/v2/entries/en/${word}`)
    .then(res => res.json()) //converting to json format

    return(res)
}

btn.addEventListener("click", (fetchAndCreateCard))

async function fetchAndCreateCard()
{
    let inpWord = document.getElementById("inp-word").value;
    const data = await dictionaryFn(inpWord)
    console.log(data)

result.innerHTML = 
`<div class="card">
    <div class="word">
        <h3>${inpWord}</h3>
        <span>
        <audio class="audio" controls src="${data[0].phonetics[0].audio}"></audio>
        </span>
    </div>
    <div class="details">
        <p>${data[0].meanings[0].partOfSpeech}</p>
        <p>/${data[0].phonetic}/</p>
    </div>
    <p class="word-meaning">
        ${data[0].meanings[0].definitions[0].definition}
    </p>
    <p class="word-example">
        ${data[0].meanings[0].definitions[0].example || ""}
    </p>
</div>`;

}







