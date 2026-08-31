const glow =
document.querySelector(".cursor-glow");

document.addEventListener(
"mousemove",
e=>{
glow.style.left=e.clientX+"px";
glow.style.top=e.clientY+"px";
}
);

function saveHTML(){

const html =
document.documentElement.outerHTML;

const blob =
new Blob(
[html],
{type:"text/html"}
);

const a =
document.createElement("a");

a.href =
URL.createObjectURL(blob);

a.download =
"portfolio.html";

a.click();
}

function saveScreen(){

html2canvas(
document.querySelector("#captureArea"),
{
scale:2
}
)
.then(canvas=>{

const link =
document.createElement("a");

link.download =
"portfolio.png";

link.href =
canvas.toDataURL();

  const colorPicker =
document.getElementById(
"themeColor"
);

colorPicker.addEventListener(
"input",
e=>{

document.documentElement
.style.setProperty(
"--accent",
e.target.value
);

}
);

document
.getElementById(
"imageUpload"
)
.addEventListener(
"change",
e=>{

const file =
e.target.files[0];

if(!file) return;

const reader =
new FileReader();

reader.onload =
ev=>{

document
.getElementById(
"avatar"
)
.src =
ev.target.result;

};

reader.readAsDataURL(file);

}
);

function saveProfile(){

const data={

name:
document.getElementById("name")
.innerText,

title:
document.getElementById("title")
.innerText,

description:
document.getElementById("description")
.innerText,

image:
document.getElementById("avatar")
.src,

color:
getComputedStyle(
document.documentElement
)
.getPropertyValue(
"--accent"
)

};

const blob=
new Blob(
[
JSON.stringify(
data,
null,
2
)
],
{
type:"application/json"
}
);

const a=
document.createElement("a");

a.href=
URL.createObjectURL(blob);

a.download=
"profile.json";

a.click();
}

function loadProfile(){

document
.getElementById(
"loadFile"
)
.click();

}

document
.getElementById(
"loadFile"
)
.addEventListener(
"change",
e=>{

const file=
e.target.files[0];

const reader=
new FileReader();

reader.onload=
ev=>{

const data=
JSON.parse(
ev.target.result
);

name.innerText=
data.name;

title.innerText=
data.title;

description.innerText=
data.description;

avatar.src=
data.image;

document
.documentElement
.style.setProperty(
"--accent",
data.color
);

themeColor.value=
data.color;

};

reader.readAsText(file);

}
);

link.click();

});
}
