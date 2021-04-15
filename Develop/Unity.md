# Unity

### Buscar Objetos

1. Buscar elementos por nombre en la jerarquia, padre a hijo
````csharp
 btnPlay.transform.Find("icon").gameObject.SetActive(false);
````

### Buscar Clases

###### Buscar funcion por clase
````csharp
FindObjectOfType<UIController>().HideMenu();
````

### Modificar Objetos
###### Aplicar cambio de una propiedad a un objeto

````csharp
 back.GetComponent<Image>().DOFade(0.80f, .25f).OnComplete(()=>{});
````

### Event listener 
##### Eventro de boton desde jerarquia de clase
```csharp
buttonGame.transform.Find("buttonCollection").gameObject.GetComponent<Button>().onClick.AddListener(() =>
    {
      //StartCoroutine(ShowGamesCollection(item.id_coleccion));
      print("Clickeado");
    });
```