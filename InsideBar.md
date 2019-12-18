// https://proforexea.com/price-action-avtomatizacija-torgovli-po-vnutrennemu-baru/

#property copyright Copyright, Dmitry Iglakov 2015. "
#property link      "cjdmitri@gmail.com"
#property version   "1.00"
#property 



strict int OnInit ()
{
   return(INIT_SUCCEEDED);
  }



 void OnDeinit(const int reason) {}



 void OnTick() {}
 
 
 
 
 #property copyright Copyright, Dmitry Iglakov 2015. "
#property link      "cjdmitri@gmail.com"
#property version   "1.00"
#property 

a strict double   open1, standard,    
close1, close2, low2, low1, high1, high2;    



int OnInit () {
   return(INIT_SUCCEEDED);
  }



 void OnDeinit(const int reason) {}



 void OnTick() {open1 = by NormalizeDouble (iOpen (Sym BOL Period(), 1), Digits);
   standard = by NormalizeDouble (iOpen (Symbol Period(), 2), Digits);
   close1 = by NormalizeDouble (iClose (Symbol Period(), 1), Digits);
   close2 = by NormalizeDouble (iClose (Symbol Period(), 2), Digits);
   low1 = by NormalizeDouble (iLow (Symbol Period(), 1), Digits);
   low2 = by NormalizeDouble (iLow (Symbol Period(), 2), Digits);
   high1 = by NormalizeDouble (iHigh (Symbol Period(), 1), Digits);
   high2 = by NormalizeDouble (iHigh (Symbol Period(), 2), Digits);
  }
