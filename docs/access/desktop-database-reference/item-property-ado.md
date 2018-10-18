---
<<<<<<< Titre tête : élément propriété (ADO) TOCTitle : élément de propriété (ADO) === titre : Item, propriété (ADO) TOCTitle : Item, propriété (ADO)
>>>>>>> Master ms:assetid : 793c305f-0e5b-a529-e21f-b7ab0843ed49 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249499(v=office.15) ms:contentKeyID : ms.date 48545767 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="item-property-ado"></a>Item, propriété (ADO)
=======
# <a name="item-property-ado"></a>Item, propriété (ADO)
>>>>>>> master

**S’applique à**: Access 2013 | Office 2013

Indique membre spécifique d'une collection, par son nom ou son nombre ordinal.

## <a name="syntax"></a>Syntaxe

Définir*l’objet* = *collection*. Item (Index)

<<<<<<< Tête
## <a name="return-value"></a>Valeur renvoyée
=======
## <a name="return-value"></a>Valeur renvoyée
>>>>>>> master

Renvoie une référence à un objet.

## <a name="parameters"></a>Paramètres

- *Index*

- Une expression **Variant** qui correspond soit au nom, soit au nombre ordinal d'un objet dans une collection.

## <a name="remarks"></a>Remarques

Utilisez la propriété **Item** pour renvoyer un objet spécifique dans une collection. Si **l’élément** ne peut pas trouver un objet dans la collection correspondant à l’argument *Index* , une erreur se produit. Si la collection ne prend pas en charge les objets nommés, utilisez des nombres ordinaux comme références.

La propriété **Item** est la propriété par défaut de toutes les collections ; les formes de syntaxe suivantes sont donc interchangeables :

```vb
    collection.Item (Index)
    collection (Index)
```
