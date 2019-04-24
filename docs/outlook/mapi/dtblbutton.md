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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a8fa683fecd59ec813fee0c15d5b4f08084c645d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338310"
---
# <a name="dtblbutton"></a>DTBLBUTTON

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des informations sur un contrôle bouton pour une boîte de dialogue construite à partir d'une table d'affichage.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Macro connexe:  <br/> |[SizedDtblButton](sizeddtblbutton.md) <br/> |
   
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
  
> Position en mémoire de la chaîne de caractères qui est affichée sur le bouton.
    
 **ulFlags**
  
> Masque de des indicateurs utilisé pour désigner le format de l'étiquette désignée par le membre **ulbLpszLabel** . L'indicateur suivant peut être défini: 
    
MAPI_UNICODE 
  
> L'étiquette est au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, l'étiquette est au format ANSI.
    
 **ulPRControl**
  
> Balise de propriété pour une propriété de type PT_OBJECT qui implémente l'interface [IMAPIControl](imapicontroliunknown.md) . Lorsque l'utilisateur clique sur le bouton, MAPI appelle la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) pour l'implémentation [IMAPIProp](imapipropiunknown.md) de la table d'affichage afin de récupérer cette propriété. 
    
## <a name="remarks"></a>Remarques

Une structure **DTBLBUTTON** décrit un bouton qui permet à un utilisateur de commencer une opération lorsqu'un utilisateur clique dessus. En règle générale, le fait de cliquer sur un bouton entraîne l'affichage d'une boîte de dialogue modale ou d'une tâche de programmation. Les fournisseurs de services peuvent implémenter n'importe quoi par le biais d'un contrôle de bouton. Si le bouton est censé effectuer une tâche basée sur les valeurs d'autres contrôles, ces contrôles doivent avoir défini l'indicateur DT_SET_IMMEDIATE. 
  
Le membre **ulbLpszLabel** est la position en mémoire de la chaîne de caractères qui est affichée sur le bouton. Les fournisseurs de services peuvent ajouter un caractère&amp;perluète () pour indiquer un accélérateur Windows dans l'étiquette du bouton. Appuyer sur une touche d'accès rapide revient à cliquer sur le bouton. 
  
Le membre **ulPRControl** décrit une propriété Object qui, lorsqu'elle est ouverte avec la méthode **IMAPIProp:: OpenProperty** , renvoie un pointeur vers un objet Control. L'implémentation d'un objet Control qui prend en charge l'interface **IMAPIControl** permet d'étendre l'ensemble de fonctionnalités MAPI et de définir l'opération ou la tâche qui se produit lorsque l'utilisateur clique sur le bouton. **IMAPIControl** fournit deux méthodes pour manipuler des boutons: [GetState](imapicontrol-getstate.md) pour désactiver ou activer des boutons et [activer](imapicontrol-activate.md) pour gérer les clics de bouton. 
  
Pour une vue d'ensemble des tables d'affichage, voir [afficher les tables](display-tables.md). Pour plus d'informations sur l'implémentation d'une table d'affichage, voir [Implementing a Display table](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

