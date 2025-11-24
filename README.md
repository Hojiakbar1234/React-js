import React, { useState } from "react";
import "./App.css";

function App() {

  // 1 — Matnni almashtirish
  const [text1, setText1] = useState("Assalomu aleykum");
  const toggleText1 = () => {
    setText1(text1 === "Assalomu aleykum" ? "Valeykum assalom" : "Assalomu aleykum");
  };

  // 2 — Rang almashtirish
  const [bgColor, setBgColor] = useState("pink");
  const toggleColor = () => {
    setBgColor(bgColor === "pink" ? "red" : "pink");
  };

  // 3 — 2 ta tugma orqali matn boshqaruv
  const [job, setJob] = useState("Frontend Developer");

  // 4 — Parolni ko‘rsatish / yashirish
  const [showPass, setShowPass] = useState(false);
  const [password] = useState("123456");
  const togglePassword = () => {
    setShowPass(!showPass);
  };

  // 5 — Tilni almashtirish
  const [lang, setLang] = useState("hello");
  const toggleLang = () => {
    setLang(lang === "hello" ? "salom" : "hello");
  };

  // 6 — Katta-kichik harf
  const [harf, setHarf] = useState("frontend");
  const toggleCase = () => {
    setHarf(harf === "frontend" ? "FRONTEND" : "frontend");
  };

  // 7 — Div hajmini o‘zgartirish
  const [boxSize, setBoxSize] = useState("100px");
  const toggleSize = () => {
    setBoxSize(boxSize === "100px" ? "200px" : "100px");
  };

  // 8 — Tugma matnini almashtirish
  const [btnText, setBtnText] = useState("Yoqish");
  const toggleBtn = () => {
    setBtnText(btnText === "Yoqish" ? "O‘chirish" : "Yoqish");
  };

  return (
    <div style={{ padding: "30px" }}>

      <h1> 1. Matnni almashtirish</h1>
      <h2>{text1}</h2>
      <button onClick={toggleText1}>Almashtir</button>
      

      <h1>2. Rang almashtiruvchi funksiya</h1>
      <div style={{ width: "150px", height: "80px", background: bgColor }}></div>
      <button onClick={toggleColor}>Rangni o‘zgartir</button>
      

      <h1> 3. Ikki tugmali matn boshqaruv</h1>
      <h2>{job}</h2>
      <button onClick={() => setJob("React Developer")}>React Developer</button>
      <button onClick={() => setJob("JavaScript Developer")}>JavaScript Developer</button>
     

      <h1> 4. Parolni ko‘rsat/yashirish</h1>
      <h2>{showPass ? password : "******"}</h2>
      <button onClick={togglePassword}>
        {showPass ? "Yashirish" : "Ko‘rsatish"}
      </button>
    

      <h1> 5. Tilni almashtirish</h1>
      <h2>{lang}</h2>
      <button onClick={toggleLang}>Tilni o‘zgartir</button>
      

      <h1> 6. Katta/kichik harf</h1>
      <h2>{harf}</h2>
      <button onClick={toggleCase}>Harfni o‘zgartir</button>
      

      <h1> 7. Div o‘lchamini o‘zgartirish</h1>
      <div
        style={{
          width: boxSize,
          height: boxSize,
          background: "lightblue",
        }}
      ></div>
      <button onClick={toggleSize}>Hajmni o‘zgartir</button>
    

      <h1>🖲 8. Tugma matnini almashtirish</h1>
      <button onClick={toggleBtn}>{btnText}</button>
      <hr />
    </div>
  );
}

export default App;
