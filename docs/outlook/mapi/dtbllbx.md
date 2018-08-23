---
title: DTBLLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLBX
api_type:
- COM
ms.assetid: 971b4837-6823-4f28-9803-3c22b2ec091f
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 35e19a4281c46ae7c2b5cbd76c1ecea35bf87665
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569763"
---
# <a name="dtbllbx"></a>DTBLLBX

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Décrit une liste qui sera utilisée dans une boîte de dialogue qui est générée à partir d’un tableau d’affichage.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLLBX
{
  ULONG ulFlags;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLLBX, FAR *LPDTBLLBX

```

## <a name="members"></a>Members

 **ulFlags**
  
> Masque de bits d’indicateurs utilisés pour supprimer une barre de défilement horizontal ou vertical dans la liste. Les indicateurs suivants peuvent être définis :
    
MAPI_NO_HBAR 
  
> Aucune barre de défilement horizontale ne doit être affichée dans la liste.
    
MAPI_NO_VBAR 
  
> Aucune barre de défilement verticale ne doit être affichée dans la liste.
    
 **ulPRSetProperty**
  
> Balise de propriété pour une propriété d’un type quelconque. Cette propriété est une des colonnes de la table identifiée par le membre **ulPRTableTable** . 
    
 **ulPRTableName**
  
> Balise de propriété pour une propriété de tableau de type PT_OBJECT qui peuvent être ouverts à l’aide d’un **OpenProperty** appeler. Le nombre de colonnes pour la table varie selon que la liste est une liste à sélection unique ou multiple. Si le membre **ulPRSetProperty** est défini sur **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), la liste permet à sélection multiple.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLLBX** décrit un contrôle qui est utilisé pour afficher plusieurs éléments et permettent à un utilisateur de sélectionner une ou plusieurs des éléments de liste. 
  
Le membre **ulPRSetProperty** et **ulPRTableName** membre collaborent ; Lorsque vous sélectionnez une valeur de la table, il est réécrit dans **ulPRSetProperty** lorsque la boîte de dialogue est fermée. 
  
La valeur flags indique si une barre de défilement horizontale ou verticale doit être affichée avec la liste. La valeur par défaut est d’avoir des types de défilement barres s’affichent si cela est nécessaire. Fournisseurs de services peuvent définir MAPI_NO_HBAR pour supprimer une barre de défilement horizontale et MAPI_NO_VBAR pour supprimer une barre de défilement verticale. 
  
Les membres de balise de deux propriété travaillent ensemble pour afficher les valeurs dans la liste et définir les propriétés correspondantes lorsqu’un élément dans la liste est sélectionné. Lorsque tout d’abord, MAPI affiche la liste, il appelle la méthode **OpenProperty** de l’implémentation **IMAPIProp** pour récupérer la table identifiée dans le membre **ulPRTableName** . Le nombre de colonnes dans le tableau dépend de la valeur du membre **ulPRSetProperty** . Si **ulPRSetProperty** est défini sur **PR_NULL**, la liste est une liste de sélection de plusieurs basée sur un objet qui contient les destinataires, comme un conteneur de carnet d’adresses, une table de destinataires pour un message ou un tableau de contenu de liste de distribution. 
  
Un objet table pour une liste de sélection multiple doit inclure les colonnes suivantes :
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
 **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
  
 **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) et un maximum de cinq autres propriétés de type chaîne à valeurs multiples peut également être affiché avec les trois colonnes requises. 
  
Si le membre **ulPRSetProperty** n’est pas défini sur **PR_NULL**, la liste est une liste à sélection unique. La valeur initiale de **ulPRSetProperty** détermine la première ligne sélectionnée. Lorsqu’un utilisateur sélectionne une des lignes, le membre **ulPRSetProperty** est défini à la valeur sélectionnée et cette valeur est réécrit dans l’implémentation d’interface de propriété avec un appel à [IMAPIProp::SetProps](imapiprop-setprops.md). 
  
Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md). Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

