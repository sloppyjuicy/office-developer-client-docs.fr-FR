---
title: Implémentation d’objets dans C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 24fc4d78-726d-40ff-bad2-25dc298bd51a
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 71a8dc6472051e72d990a5c5d6f026ae63f1df25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784193"
---
# <a name="implementing-objects-in-c"></a>Implémentation d’objets dans C

**S’applique à**: Outlook 
  
Applications clientes et des fournisseurs de services écrits en C définissent les objets MAPI en créant une structure de données et un tableau de pointeurs fonction triée appelé une table de fonctions virtuelles ou vtable. Un pointeur vers la vtable doit être le premier membre de la structure de données.
  
Dans la vtable lui-même, il existe un pointeur pour chaque méthode dans chaque interface pris en charge par l’objet. L’ordre des pointeurs doit respecter l’ordre des méthodes de l’interface publiée dans le fichier d’en-tête Mapidefs.h. Chaque pointeur de fonction vtable est définie à l’adresse de l’implémentation de la méthode réelle. En C++, le compilateur définit automatiquement la vtable. C, il n’existe pas. 
  
L’illustration suivante montre comment cela fonctionne. La zone à l’extrême gauche représente un client qui a besoin d’utiliser un objet de fournisseur de services. Par le biais de la session, le client obtient un pointeur vers l’objet, **lpObject**. Vtable apparaît en premier dans l’objet suivi par des méthodes et des données privées. Le pointeur vtable pointe vers la vtable réelle, qui contient des pointeurs à chacun des implémentations des méthodes dans l’interface. 
  
**Implémentation de l’objet**
  
![Implémentation de l’objet] (media/amapi_42.gif "Implémentation de l’objet")
  
L’exemple de code suivant montre comment un fournisseur de services C définir un objet état simple. Le premier membre est le pointeur vtable ; le reste de l’objet est composé des membres de données. 
  
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

Étant donné que cet objet est un objet d’état, vtable comprend des pointeurs vers des implémentations de chacune des méthodes dans le [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, ainsi que des pointeurs vers des implémentations de chacune des méthodes dans les interfaces de base — **IUnknown **et **IMAPIProp**. L’ordre des méthodes vtable correspond à l’ordre spécifié comme défini dans le fichier d’en-tête Mapidefs.h.
  
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

Clients et fournisseurs de services écrits en C des objets indirectement via la vtable et ajoutez un pointeur d’objet en tant que le premier paramètre de chaque appel. Chaque appel à une méthode d’interface MAPI nécessite un pointeur vers l’objet appelé comme premier paramètre. C++ définit un pointeur spécial appelé le pointeur **this** à cet effet. Le compilateur C++ ajoute implicitement le pointeur **this** comme premier paramètre à chaque appel de méthode. C il n’existe aucun pointeur de ce type ; Il doit être explicitement ajoutée. 
  
Le code suivant montre comment un client peut effectuer un appel à une instance de MYSTATUSOBJECT :
  
```C
lpMyObj->lpVtbl->ValidateState(lpMyObj, ulUIParam, ulFlags);
 
```

## <a name="see-also"></a>Voir aussi

- [Implémentation d’objets MAPI](implementing-mapi-objects.md)

