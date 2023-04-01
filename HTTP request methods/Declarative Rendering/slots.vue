Oprócz przekazywania danych przez rekwizyty, komponent nadrzędny może również przekazywać dziecku fragmenty szablonu za pośrednictwem slotów :

<ChildComp>
    This is some slot content!
  </ChildComp>

W komponencie potomnym może renderować zawartość gniazda z elementu nadrzędnego, używając elementu <slot>jako gniazda:

<!-- in child template -->
<slot/>