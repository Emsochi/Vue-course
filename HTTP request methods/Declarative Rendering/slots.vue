Oprócz przekazywania danych przez rekwizyty, komponent nadrzędny może również przekazywać dziecku fragmenty szablonu za pośrednictwem slotów :

<ChildComp>
    This is some slot content!
  </ChildComp>

W komponencie potomnym może renderować zawartość gniazda z elementu nadrzędnego, używając elementu <slot>jako gniazda:

<!-- in child template -->
<slot/>

Treść w <slot>punkcie sprzedaży będzie traktowana jako treść „zastępcza”: 
zostanie wyświetlona, ​​jeśli rodzic nie przekazał żadnej zawartości gniazda:

<slot>Fallback content</slot>

Obecnie nie przekazujemy żadnej zawartości boksu do <ChildComp>, więc powinieneś zobaczyć zawartość zastępczą. 
Udostępnijmy dziecku trochę zawartości gniazda, korzystając ze msgstanu rodzica.