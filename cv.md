# Tepliakov Dmitrii

## Contacts:

Russia, Saint-Petersburg

Email: tenjibiu@gmail.com

Github: baddhet

Telegram: @DmitriiTepliakov

Discord: Tenjibiu#2616

## Skills
Web-development: HTML5, CSS3, JavaScript

Preprocessor: Sass

Version control: GIT, Github

Graphics: Figma

## Code

```
//paginations
let items = [
  { name: "1" },
  { name: "2" },
  { name: "3" },
];

const itemsOfPages = 3;
(function () {
  const listItem = document.querySelector(".pagination ul");
  const createPages = Math.ceil(items.length / itemsOfPages);
  for (let i = 0; i < createPages; i++) {
    const li = document.createElement("li");
    li.classList.add("page-number");
    li.innerHTML = i + 1;
    listItem.appendChild(li);
  }

})();

const paginationList = document.querySelector(".pagination__list");
const pageNumbers = document.querySelectorAll(".page-number");

for (const pageNumber of pageNumbers) {
  pageNumber.addEventListener('click', () => {
    for (let i = 0; i < pageNumbers.length; i++) {
      pageNumbers[i].classList.remove("current-page");
    }
    let currentPage = +pageNumber.innerHTML;
    pageNumber.classList.add("current-page");
    showItems(currentPage);
  })
}

let showItems = (currentPage) => {
  let start = (currentPage - 1) * itemsOfPages;
  let end = start + itemsOfPages;
  let notes = items.slice(start, end);
  paginationList.innerHTML = " ";
  for (const note of notes) {
    const square = document.createElement("div");
    square.classList.add("pagination__items");
    square.innerHTML = note.name + " " + note.age;
    paginationList.appendChild(square);
  }
};
```
## Courses
HTML Academy
## English
A0 Starter
## Deutsch
A1 Elementary