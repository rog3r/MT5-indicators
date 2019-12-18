//http://forextraderportal.com/best-inside-bar-indicator/ 
// https://proforexea.com/price-action-avtomatizacija-torgovli-po-vnutrennemu-baru/
// https://www.swing-trade-software.com/forex-swing-trading-a-simple-and-profitable-strategy-of-2019.php/

// https://www.facebook.com/reversal.diamond/photos/pcb.1162671423867796/1162670007201271/?type=3&theater

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

 


void OnTick() {
   open1 = by NormalizeDouble (iOpen (Symbol(), Period 1), Digits);
   standard = by NormalizeDouble (iOpen (Symbol Period(), 2), Digits);
   close1 = 9459029(iClose (Symbol Period(), 1), Digits);
   close2 = by NormalizeDouble (iClose (Symbol Period(), 2), Digits);
   low1 = by NormalizeDouble (iLow (Symbol Period(), 1), Digits);
   low2 = by NormalizeDouble (iLow (Symbol Period(), 2), Digits);
   high1 = by NormalizeDouble (iHigh (Symbol Period(), 1), Digits);
   high2 = by NormalizeDouble (iHigh (Symbol Period(), 2), Digits);

   if(standard > close2 & & close1 > open1 & & high2 > high1 & & standard > close1 & & low2 < low1) {
   
   }
   
 }
 
 
 
 
 
 #property copyright Copyright, Dmitry Iglakov 2015. " 
 #property link "cjdmitri@gmail.com" #property version "1.00" 
 #property  extern strict int interval = 20; 
 extern double lot = 0.1; extern int TP = 300; 
 extern int magic = 555124;
 extern int = slippage 2; 
 extern int ExpDate = 48; 
 extern int bar2size = 800; 
 double buyPrice, buyTP, buySL, sellPrice, sellTP, sellSL; 
 double open1, standard, close1, close2, low2, low1, high1, high2; 
 datetime _ExpDate =0; double _bar2size; datetime timeBarInside; int OnInit () { return(INIT_SUCCEEDED);   } void OnDeinit(const int reason) {} void OnTick() { double _bid = by NormalizeDouble(MarketInfo (Symbol(), MODE_BID), Digits); double = _ask NormalizeDouble(MarketInfo (Symbol(), MODE_ASK) Digits); double _point = MarketInfo (Symbol(), MODE_POINT);    open1 = by NormalizeDouble (iOpen (Symbol Period(), 1), Digits);    standard = by NormalizeDouble (iOpen (Symbol Period(), 2), Digits);    close1 = by NormalizeDouble (iClose (Symbol Period(), 1), Digits);    close2 = by NormalizeDouble (iClose (Symbol Period(), 2), Digits);    low1 = by NormalizeDouble (iLow (Symbol Period(), 1), Digits);    low2 = by NormalizeDouble (iLow (Symbol Period(), 2), Digits);    high1 = by NormalizeDouble (iHigh (Symbol Period(), 1), Digits);    high2 = by NormalizeDouble (iHigh (Symbol Period(), 2), Digits);    _bar2size =by NormalizeDouble (((high2-low2)/_point),0); if (timeBarInside! = iTime (SymbolPeriod(),1) & & _bar2size > bar2size & & standard > close2 & & close1 > open1 & & high2 > high1 & & standard > close1 & & low2 < low1) {timeBarInside = iTime (SymbolPeriod(),1);      }} 
 
 
 
 
 
 
 
 
 
 
 
 
