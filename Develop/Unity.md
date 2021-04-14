# Unity

### Buscar Objetos

1. Buscar elementos por nombre en la jerarquia, padre a hijo
````csharp
 btnPlay.transform.Find("icon").gameObject.SetActive(false);
````
### Buscar Clases

3. Buscar funcion por clase
````csharp
FindObjectOfType<UIController>().HideMenu();
````
### Modificar Objetos
1. Aplicar cambio de una propiedad a un objeto

````sharp
 back.GetComponent<Image>().DOFade(0.80f, .25f).OnComplete(()=>{});
````