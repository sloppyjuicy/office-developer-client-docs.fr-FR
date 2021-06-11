---
title: DTBLBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLBUTTON
api_type:
- COM
ms.assetid: 6058c78b-05d4-45a3-988c-1fbf8322125e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a8fa683fecd59ec813fee0c15d5b4f08084c645d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412785"
---
# <a name="dtblbutton"></a>DTBLBUTTON

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des informations sur un contrôle de bouton pour une boîte de dialogue conçue à partir d’un tableau d’affichage.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macro associée :  <br/> |[SizedDtblButton](sizeddtblbutton.md) <br/> |
   
```cpp
typedef struct _DTBLBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRControl;
} DTBLBUTTON, FAR *LPDTBLBUTTON;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Position en mémoire de la chaîne de caractères affichée sur le bouton.
    
 **ulFlags**
  
> Masque de bits d’indicateurs utilisé pour désigner le format de l’étiquette pointée par le membre **ulbLpszLabel.** L’indicateur suivant peut être définie : 
    
MAPI_UNICODE 
  
> L’étiquette est au format Unicode. Si l’MAPI_UNICODE n’est pas définie, l’étiquette est au format ANSI.
    
 **ulPRControl**
  
> Balise de propriété pour une propriété de type PT_OBJECT qui implémente l’interface [IMAPIControl.](imapicontroliunknown.md) Lorsque vous cliquez sur le bouton, MAPI appelle la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour l’implémentation [IMAPIProp](imapipropiunknown.md) de la table d’affichage afin de récupérer cette propriété. 
    
## <a name="remarks"></a>Remarques

Une structure **DTBLBUTTON** décrit un bouton d’un contrôle qui, lorsqu’on clique dessus, permet à un utilisateur de commencer une opération. En règle générale, le fait de cliquer sur un bouton entraîne l’affichage d’une boîte de dialogue modale ou l’appel d’une tâche par programme. Les fournisseurs de services peuvent implémenter n’importe quoi par le biais d’un contrôle de bouton. Si le bouton est censé effectuer une tâche basée sur les valeurs d’autres contrôles, ces contrôles doivent avoir DT_SET_IMMEDIATE indicateur. 
  
Le **membre ulbLpszLabel** est la position dans la mémoire de la chaîne de caractères qui s’affiche sur le bouton. Les fournisseurs de services peuvent ajouter un caractère « eter » () pour indiquer un Windows &amp; dans l’étiquette du bouton. Appuyer sur une touche d’accélérateur a le même effet que de cliquer sur le bouton. 
  
Le **membre ulPRControl** décrit une propriété d’objet qui, lorsqu’elle est ouverte avec la méthode **IMAPIProp::OpenProperty,** renvoie un pointeur vers un objet de contrôle. L’implémentation d’un objet de contrôle qui prend en charge l’interface **IMAPIControl** est un moyen d’étendre l’ensemble de fonctionnalités MAPI et de définir l’opération ou la tâche qui se produit lorsque l’utilisateur clique sur le bouton. **IMAPIControl fournit** deux méthodes de manipulation des boutons : [GetState](imapicontrol-getstate.md) pour désactiver ou activer les boutons et [Activate](imapicontrol-activate.md) pour gérer les clics de bouton. 
  
Pour une vue d’ensemble des tableaux d’affichage, voir [Afficher les tableaux.](display-tables.md) Pour plus d’informations sur l’implémentation d’un tableau d’affichage, voir [Implementing a Display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

