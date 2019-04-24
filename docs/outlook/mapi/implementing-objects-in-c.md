---
title: Implémentation des objets dans C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 24fc4d78-726d-40ff-bad2-25dc298bd51a
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 6026e697cc31545bf7ef518fcbd33ea8db48af5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310187"
---
# <a name="implementing-objects-in-c"></a>Implémentation des objets dans C

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes et les fournisseurs de services écrits en C définissent les objets MAPI en créant une structure de données et un tableau de pointeurs de fonctions ordonnées, appelés table de fonctions virtuelles ou vtable. Un pointeur vers vtable doit être le premier membre de la structure de données.
  
Dans la vtable, il existe un pointeur pour chaque méthode dans chaque interface prise en charge par l'objet. L'ordre des pointeurs doit suivre l'ordre des méthodes dans la spécification de l'interface publiée dans le fichier d'en-tête Mapidefs. h. Chaque pointeur fonction dans vtable est défini sur l'adresse de l'implémentation réelle de la méthode. En C++, le compilateur configure automatiquement le vtable. Dans C, ce n'est pas le cas. 
  
L'illustration suivante montre comment cela fonctionne. La zone située à l'extrême gauche représente un client qui doit utiliser un objet fournisseur de services. Par le biais de la session, le client obtient un pointeur vers l'objet, **lpObject**. Le vtable apparaît en premier dans l'objet suivi de données et de méthodes privées. Le pointeur vtable pointe vers le vtable réel, qui contient des pointeurs vers chacune des implémentations des méthodes dans l'interface. 
  
**Implémentation d’objet**
  
![Implémentation d'objet] (media/amapi_42.gif "Implémentation d'objet")
  
L'exemple de code suivant montre comment un fournisseur de services C peut définir un objet d'état simple. Le premier membre est le pointeur vtable; le reste de l'objet est composé de membres de données. 
  
```C
typedef struct _MYSTATUSOBJECT
{
    const STATUS_Vtbl FAR *lpVtbl;
    ULONG              cRef;
    ANOTHEROBJ        *pObj;
    LPMAPIPROP         lpProp;
    LPFREEBUFFER       lpFreeBuf;
} MYSTATUSOBJECT, *LPMYSTATUSOBJ;
 
```

Étant donné que cet objet est un objet d'État, le vtable inclut des pointeurs vers les implémentations de chacune des méthodes de l'interface [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) , ainsi que des pointeurs vers des implémentations de chacune des méthodes dans les interfaces de base — **IUnknown **et **IMAPIProp**. L'ordre des méthodes dans vtable correspond à l'ordre spécifié tel qu'il est défini dans le fichier d'en-tête Mapidefs. h.
  
```js
static const MYOBJECT_Vtbl vtblSTATUS =
{
    STATUS_QueryInterface,
    STATUS_AddRef,
    STATUS_Release,
    STATUS_GetLastError,
    STATUS_SaveChanges,
    STATUS_GetProps,
    STATUS_GetPropList,
    STATUS_OpenProperty,
    STATUS_SetProps,
    STATUS_DeleteProps,
    STATUS_CopyTo,
    STATUS_CopyProps,
    STATUS_GetNamesFromIDs,
    STATUS_GetIDsFromNames,
    STATUS_ValidateState,
    STATUS_SettingsDialog,
    STATUS_ChangePassword,
    STATUS_FlushQueues
};
 
```

Les clients et fournisseurs de services écrits en C utilisent les objets indirectement via vtable et ajoutent un pointeur d'objet comme premier paramètre dans chaque appel. Chaque appel à une méthode d'interface MAPI nécessite un pointeur vers l'objet appelé comme premier paramètre. C++ définit un pointeur spécial appelé « **This** pointeur» à cet effet. Le compilateur C++ ajoute implicitement le pointeur **This** comme premier paramètre à chaque appel de méthode. En C, il n'y a pas de pointeur de ce type; il doit être ajouté explicitement. 
  
Le code suivant montre comment un client peut effectuer un appel à une instance de MYSTATUSOBJECT:
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a>Voir aussi

- [Implémentation d'objets MAPI](implementing-mapi-objects.md)

