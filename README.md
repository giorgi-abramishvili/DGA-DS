<h1><b>
საქართველოს ციფრული სერვისების დიზაინის სისტემა
</b></h1>
ეს readme ფაილი Github-ზე შეიცავს ინფორმაციას აიკონებისა და ფონტების შესახებ, ასევე ინსტრუქციებს მათი პროექტში გამოყენების შესახებ. ის ასევე იძლევა რეკომენდაციებს ხელმისაწვდომობის სტანდარტებზე, როგორიცაა სემანტიკური HTML-ის გამოყენება, სურათების ალტერნატიული ტექსტი, კლავიატურის ხელმისაწვდომობა და ARIA როლები და ატრიბუტები. ის ასევე შეიცავს ბმულებს რესურსებისა და ხელმისაწვდომობის ინსტრუმენტების მხარდასაჭერად, რათა უზრუნველყოს ინტერფეისის ხელმისაწვდომობა ყველა მომხმარებლისთვის.

<h2><b>საფუძვლები</b></h2>

<h3>აიკონები</h3>
Material Symbols მოიცავს სხვადასხვა კატეგორიის აიკონების მრავალფეროვნებას, მათ შორის სოციალური მედიის, ნავიგაციის და სხვა. ყველა აიკონი უფასოა გამოსაყენებლად თანდართული ლიცენზიის პირობების შესაბამისად.

თქვენს პროექტში აიკონების გამოსაყენებლად, გადადით <a href="https://fonts.google.com/icons">Material Symbols guide</a>_ის ლინკზე და შეიტანეთ იგი თქვენს პროექტში.

<h3>ფონტები</h3>
Noto Sans Georgian არის არამოდულირებული (“sans serif”) დიზაინი ევროპული დამწერლობის ტექსტებისთვის. იგი გამოირჩევა როგორც სტილის ასევე ტიპოგრაფიის მრავალფეროვნებით, რაც იმას ნიშნავს რომ შესაძლებელია ერთი ფონტით დაწეროთ მინიმუმ ორ ენაზე.

თქვენს პროექტში შრიფტის გამოსაყენებლად, უბრალოდ გადმოწერეთ შესაბამისი ფაილები <a href="https://fonts.google.com/noto/specimen/Noto+Sans+Georgian">Noto Sans Georgian</a>  და დაამატეთ ისინი თქვენი პროექტის დირექტორიაში. შემდეგ შეგიძლიათ ჩართოთ შრიფტი თქვენს CSS-ში @font-face წესის გამოყენებით.

<i>მხედრულიდან მთავრულზე გადაყვანისთვის CSS ში შესაბამის ხაზზე მიუთითეთ</i>

``` CSS
font-variant-caps: all-petite-caps;

```

<h2><b>ხელმისააწვდომობა</b></h2>
<h3>ხელმისაწვდომობის სტანდარტები</h3>
ხელმისაწვდომობა მნიშვნელოვანი საკითხია ნებისმიერი პროექტისთვის, რადგან ის უზრუნველყოფს, რომ ყველა მომხმარებელს, განურჩევლად შესაძლებლობებისა თუ შეზღუდული შესაძლებლობისა, შეუძლია წვდომა და გამოიყენოს თქვენი შინაარსი. აქ მოცემულია რამდენიმე ძირითადი მითითება და წესი, რომლებიც უნდა დაიცვათ ხელმისაწვდომი ვებ აპლიკაციების დიზაინისა და შემუშავებისას:

<h3>გამოიყენეთ სემანტიკური HTML</h3>
სემანტიკური HTML არის HTML ელემენტების გამოყენების პრაქტიკა მათი დანიშნულებისამებრ, როგორიცაა h1 სათაურებისთვის და p აბზაცებისთვის. ეს არა მხოლოდ ხდის თქვენს კოდს უფრო წაკითხვასა და შენარჩუნებას, არამედ ეხმარება დამხმარე ტექნოლოგიებს, როგორიცაა ეკრანის წამკითხველები, შინაარსის სწორად ინტერპრეტაციაში.

<b>მაგალითად</b>
``` HTML
<!DOCTYPE html>
<html>
  <head>
    <title>My Web Page</title>
  </head>
  <body>
    <header>
      <h1>Welcome to My Web Page</h1>
      <nav>
        <ul>
          <li><a href="#about">About</a></li>
          <li><a href="#services">Services</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </header>
    <main>
      <section id="about">
        <h2>About Me</h2>
        <p>Here's some information about me and what I do.</p>
      </section>
      <section id="services">
        <h2>Services</h2>
        <ul>
          <li>Service 1</li>
          <li>Service 2</li>
          <li>Service 3</li>
        </ul>
      </section>
      <section id="contact">
        <h2>Contact Me</h2>
        <p>Here's how to get in touch with me:</p>
        <ul>
          <li>Email: info@example.com</li>
          <li>Phone: 555-555-5555</li>
        </ul>
      </section>
    </main>
    <footer>
      <p>Copyright © 2023 My Web Page</p>
    </footer>
  </body>
</html>
```

<h3>მიეცით ალტერნატიული ტექსტი სურათებისთვის</h3>
უსინათლო ან მხედველობის დაქვეითებული მომხმარებლებისთვის ალტერნატიული ტექსტი (ალტ ტექსტი) იძლევა გამოსახულების აღწერას, რომლის წაკითხვაც შესაძლებელია ეკრანის მკითხველის მიერ. დარწმუნდით, რომ შეიტანეთ ალტერნატიული ტექსტი ყველა სურათისთვის თქვენს პროექტში და ის უნდა იყოს აღწერილობითი და ლაკონური.

<b>მაგალითად</b>
``` PHP
<img src="example.jpg" alt="A woman walking her dog in a park">
```

<h3>შემატეთ ხელმისაწვედომობა კლავიატურას</h3>
ყველა მომხმარებელს არ შეუძლია გამოიყენოს მაუსი ან სხვა საჩვენებელი მოწყობილობა ინტერფეისზე ნავიგაციისთვის. უზრუნველყავით კლავიატურაზე ხელმისაწდვომობის პრინციპები რათა მომხმარებლებმა შეძლონ ნავიგაცია ინტერფეისზე Tab კლავიშის გამოყენებით და ინტერაქტიული ელემენტებისთვის თვალსაჩინო ფოკუსის ინდიკატორების მიწოდებით.

<b>მაგალითად</b>
``` HTML
<button tabindex="0" onclick="myFunction()">Click me</button>
```
``` CSS
button:focus {
  outline: 2px solid blue;
}
```

<h3>გამოიყენეთ ARIA როლები და ატრიბუტები</h3>
Accessible Rich Internet Applications (ARIA) როლები და ატრიბუტები უზრუნველყოფენ დამხმარე ტექნოლოგიებისთვის დამატებით ინფორმაციას თქვენი კონტენტის შესახებ. გამოიყენეთ ARIA როლები და ატრიბუტები დამატებითი კონტექსტისა და ინფორმაციის მოსაწოდებლად, მაგრამ დარწმუნდით, რომ გამოიყენეთ ისინი სწორად და ზომიერად.

<b>მაგალითად</b>
``` HTML
<div role="button" aria-label="Open menu" tabindex="0">Menu</div>
```
<i>ამ მაგალითში გვაქვს <b>div</b> ელემენტი, რომელიც მოქმედებს როგორც ღილაკი მენიუს გასახსნელად. ჩვენ გამოვიყენეთ როლის ატრიბუტი იმის აღსანიშნავად, რომ მას აქვს ღილაკის როლი და გამოვიყენეთ <b>aria-label</b> ატრიბუტი ეკრანის წამკითხველის მომხმარებლებისთვის ღილაკის ეტიკეტის ტექსტური ალტერნატივის უზრუნველსაყოფად. დაბოლოს, ჩვენ დავამატეთ <b>tabindex</b> ატრიბუტი, რათა ღილაკი ფოკუსირებადი და კლავიატურაზე ნავიგაციური გავხადოთ <b>Tab</b> კლავიშის გამოყენებით.</i>

<caption>დამხმარე რესურსები</caption>
<ol>
  <li><a href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Annotations">Using ARIA</a></li>
  <li><a href="https://www.w3.org/TR/wai-aria/">Accessible Rich Internet Applications (ARIA)</a></li>
</ol>

<h3>ხელმისაწვდომობის ტესტი</h3>
ხელმისაწვდომობის ტესტირება მნიშვნელოვანი ნაწილია ხელმისაწვდომობის განვითარებისთვის. გამოიყენეთ ინსტრუმენტები, როგორიცაა <a href="https://www.w3.org/WAI/standards-guidelines/wcag/">ვებ-კონტენტის ხელმისაწვდომობის სახელმძღვანელო (WCAG)</a> და ავტომატური ხელმისაწვდომობის ტესტირების ხელსაწყოები, რათა დარწმუნდეთ, რომ თქვენი კონტენტი ხელმისაწვდომია ყველა მომხმარებლისთვის.
