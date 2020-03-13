<!DOCTYPE html>
<html>

<head>
   <title>Shopping Cart</title>
   <meta charset="utf-8">
   <meta name="viewport" content="width=device-width, initial-scale=1">
   <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css">
   <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.11.2/css/all.css" rel="stylesheet" />
   <link href="style.css" rel="stylesheet">
</head>

<body>

   <section>
      <div class="container">
         <div class="cart">
            <div class="col-md-12 col-lg-10 mx-auto">
               <div class="cart-item">
                  <div class="row">
                     <div class="col-md-7 center-item">
                        <img src="images/product-1.png" alt="">
                        <h5>iPhone 11 128GB Black</h5>
                     </div>

                     <div class="col-md-5 center-item">
                        <div class="input-group number-spinner">
                           <button id="minus" class="btn btn-default"><i class="fas fa-minus"></i></button>
                           <input id="mobile"  type="text" class="form-control text-center" value="1">
                           <button id="plus" class="btn btn-default"><i class="fas fa-plus"></i></button>
                        </div>
                        
                        <h5>$ <span id="price">1219</span></h5>
                        <img src="images/remove.png" alt="" class="remove-item">
                     </div>
                  </div>
               </div>

               <div class="cart-item">
                  <div class="row">
                     <div class="col-md-7 center-item mx-auto">
                        <img src="images/product-2.png" alt="">
                        <h5>iPhone 11 Silicone Case - Black</h5>
                     </div>
                     <div class="col-md-5 center-item">
                        <div class="input-group number-spinner">
                           <button id="minus2" class="btn btn-default"><i class="fas fa-minus"></i></button>
                           <input id="Case" type="text" class="form-control text-center" value="1">
                           <button id="plus2" class="btn btn-default"><i class="fas fa-plus"></i></button>
                        </div>
                        <h5>$ <span id="cprice">59</span></h5>
                        <img src="images/remove.png" alt="" class="remove-item">
                     </div>
                  </div>
               </div>

               <div class="cart-item">
                  <div class="row">

                     <div class="col-md-8">
                        <h5>Subtotal: </h5>
                        <h5>Tax:</h5>
                        <h5>Total:</h5>
                     </div>

                     <div class="col-md-4 status">
                        <h5>$ <span id="Subtotal">1,278</span></h5>
                        <h5>$<span id="tax">0</span></h5>
                        <h5>$ <span id="Tamount">1,278</span></h5>
                     </div>
                  </div>
               </div>
               <div class="col-md-12 pt-4 pb-4">
                  <button id="check" type="button" class="btn btn-success check-out">Check Out</button>
               </div>
            </div>
         </div>
      </div>


   </section>




    <script>



// jokon mobile a minus click korba
const minusBtn = document.getElementById("minus");
minusBtn.addEventListener("click", function(){


// mobile value k Float korba
const mobile = document.getElementById("mobile").value;
const mobilenumber = parseFloat(mobile);


// 1 kore komar joono print diba
const update = mobilenumber - 1;
document.getElementById("mobile").value = update;


// price ar innertext ta k parsefloat kore number a print korba 
const price = document.getElementById("price").innerText;
const pricenumber = parseFloat(price);


// 1219 minus ar modde update hobbe
const updateprice = pricenumber - 1219;
document.getElementById("price").innerText = updateprice;


// prothom a total ta ber kora jonno cover+subtotal k parse float korba
// then total a print diba 
const cprice = document.getElementById("cprice").innerText;
const cpricenumber = parseFloat(cprice)

const Subtotal = document.getElementById("Subtotal").innerText;
const Subtotalnumber = parseFloat(Subtotal);

const total = updateprice + cpricenumber;
document.getElementById("Subtotal").innerText = total;


// abr same tex 1ta id niba + mot amonunt id ta innertext parseFloat korba 
// then new total2 ba jokon nam a man print diba
const tax = document.getElementById("tax").innerText;
const taxnumber = parseFloat(tax);

const Tamount = document.getElementById("Tamount").innerText;
const Tamountnumber = parseFloat(Tamount);

const total1 = total + taxnumber ;
document.getElementById("Tamount").innerText = total1;

})





 // jokon mobile a plus click korba
 const plusBtn = document.getElementById("plus");
plusBtn.addEventListener("click", function(){


// mobile value k Float korba
const mobile = document.getElementById("mobile").value;
const mobilenumber = parseFloat(mobile);


// 1 kore berbe joono print diba
const update = mobilenumber + 1;
document.getElementById("mobile").value = update;


// price ar innertext ta k parsefloat kore number a print korba 
const price = document.getElementById("price").innerText;
const pricenumber = parseFloat(price);


// 1219 + ar modde update hobbe
const updateprice = pricenumber + 1219;
document.getElementById("price").innerText = updateprice;


// prothom a total ta ber kora jonno cover+subtotal k parse float korba
// then total a print diba 
const cprice = document.getElementById("cprice").innerText;
const cpricenumber = parseFloat(cprice)

const Subtotal = document.getElementById("Subtotal").innerText;
const Subtotalnumber = parseFloat(Subtotal);

const total = updateprice + cpricenumber;
document.getElementById("Subtotal").innerText = total;


// abr same tex 1ta id niba + mot amonunt id ta innertext parseFloat korba 
// then new total2 ba jokon nam a man print diba
const tax = document.getElementById("tax").innerText;
const taxnumber = parseFloat(tax);

const Tamount = document.getElementById("Tamount").innerText;
const Tamountnumber = parseFloat(Tamount);

const total1 = total + taxnumber ;
document.getElementById("Tamount").innerText = total1;

})



// - click
 const minus2Btn = document.getElementById("minus2");
minus2Btn.addEventListener("click", function(){


// case 
const Case = document.getElementById("Case").value;
const Casenumber = parseFloat(Case);

const updateCasenumber = Casenumber - 1;
document.getElementById("Case").value = updateCasenumber;

//case price
const cprice = document.getElementById("cprice").innerText;
const cpriceNumber = parseFloat(cprice);


const updatecprice = cprice - 59;
document.getElementById("cprice").innerText = updatecprice;




//total ber hobbe 
const price = document.getElementById("price").innerText;
const pricenumber = parseFloat(price)

const Subtotal = document.getElementById("Subtotal").innerText;
const Subtotalnumber = parseFloat(Subtotal);

const total = updatecprice + pricenumber;
document.getElementById("Subtotal").innerText = total;





// sub total
const tax = document.getElementById("tax").innerText;
const taxnumber = parseFloat(tax);

const Tamount = document.getElementById("Tamount").innerText;
const Tamountnumber = parseFloat(Tamount);

const total1 = total + taxnumber ;
document.getElementById("Tamount").innerText = total1;

})




// + click
const plus2Btn = document.getElementById("plus2");
plus2Btn.addEventListener("click", function(){


// mobile value k Float korba
const Case = document.getElementById("Case").value;
const Casenumber = parseFloat(Case);


// 1 kore berbe joono print diba
const update = Casenumber + 1;
document.getElementById("Case").value = update;


// price ar innertext ta k parsefloat kore number a print korba 
const cprice = document.getElementById("cprice").innerText;
const cpricenumber = parseFloat(cprice);


// 1219 + ar modde update hobbe
const updatecprice = cpricenumber + 59;
document.getElementById("cprice").innerText = updatecprice;




//total ber hobbe 
const price = document.getElementById("price").innerText;
const pricenumber = parseFloat(price)

const Subtotal = document.getElementById("Subtotal").innerText;
const Subtotalnumber = parseFloat(Subtotal);

const total = updatecprice + pricenumber;
document.getElementById("Subtotal").innerText = total;





// sub total
const tax = document.getElementById("tax").innerText;
const taxnumber = parseFloat(tax);

const Tamount = document.getElementById("Tamount").innerText;
const Tamountnumber = parseFloat(Tamount);

const total1 = total + taxnumber ;
document.getElementById("Tamount").innerText = total1;

})

    </script>
</body>
</html>
