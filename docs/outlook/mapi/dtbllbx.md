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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2bff20af2b3e9ea4e203e38ae38a8bc19074a727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438567"
---
# <a name="dtbllbx"></a>DTBLLBX

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une liste qui sera utilisée dans une boîte de dialogue qui est conçue à partir d’un tableau d’affichage.
  
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

## <a name="members"></a>Membres

 **ulFlags**
  
> Masque de bits des indicateurs utilisés pour éliminer une barre de défilement horizontale ou verticale de la liste. Les indicateurs suivants peuvent être définies :
    
MAPI_NO_HBAR 
  
> Aucune barre de défilement horizontale ne doit être affichée avec la liste.
    
MAPI_NO_VBAR 
  
> Aucune barre de défilement verticale ne doit être affichée avec la liste.
    
 **ulPRSetProperty**
  
> Balise de propriété pour une propriété de n’importe quel type. Cette propriété est l’une des colonnes du tableau identifiées par le **membre ulPRTableTable.** 
    
 **ulPRTableName**
  
> Balise de propriété pour une propriété de table de type PT_OBJECT qui peut être ouverte à l’aide d’un **appel OpenProperty.** Le nombre de colonnes que le tableau doit avoir varie selon que la liste est une liste de sélection unique ou multiple. Si le **membre ulPRSetProperty** est PR_NULL **(** [PidTagNull](pidtagnull-canonical-property.md)), la liste autorise la sélection multiple.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLLBX** décrit une liste un contrôle qui est utilisé pour afficher plusieurs éléments et permet à un utilisateur de sélectionner un ou plusieurs des éléments. 
  
Le **membre ulPRSetProperty** et le membre **ulPRTableName** fonctionnent ensemble . lorsqu’une valeur est choisie dans le tableau, elle est écrite dans **ulPRSetProperty** lorsque la boîte de dialogue est rejetée. 
  
La valeur des indicateurs indique si une barre de défilement horizontale ou verticale doit être affichée avec la liste. Par défaut, des types de barres de défilement doivent apparaître si nécessaire. Les fournisseurs de services peuvent définir des MAPI_NO_HBAR pour supprimer une barre de défilement horizontale et MAPI_NO_VBAR supprimer une barre de défilement verticale. 
  
Les deux membres de balise de propriété fonctionnent ensemble pour afficher les valeurs dans la liste et définir les propriétés correspondantes lorsqu’un élément de la liste est sélectionné. Lorsque MAPI affiche la liste pour la première fois, il appelle la méthode **OpenProperty** de l’implémentation **IMAPIProp** pour récupérer la table identifiée dans le membre **ulPRTableName.** Le nombre de colonnes dans le tableau dépend de la valeur du **membre ulPRSetProperty.** Si **ulPRSetProperty** est définie sur **PR_NULL**, la liste est une liste de sélections multiples basée sur un objet qui contient des destinataires, tels qu’un conteneur de carnet d’adresses, une table des destinataires pour un message ou une table de contenu de liste de distribution. 
  
Un tableau pour une liste de sélections multiples doit inclure les colonnes suivantes :
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
 **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
  
 **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) et un maximum de cinq autres propriétés de chaîne à valeurs multiples peuvent également être affichés avec les trois colonnes requises. 
  
Si le **membre ulPRSetProperty** n’est pas PR_NULL **,** la liste est une liste de sélection unique. La valeur initiale de **ulPRSetProperty** détermine la première ligne sélectionnée. Lorsqu’un utilisateur sélectionne l’une des lignes, le membre **ulPRSetProperty** est définie sur la valeur sélectionnée et cette valeur est écrite dans l’implémentation de l’interface de propriétés avec un appel à [IMAPIProp::SetProps](imapiprop-setprops.md). 
  
Pour obtenir une vue d’ensemble des tableaux d’affichage, voir [Tableaux d’affichage.](display-tables.md) Pour plus d’informations sur l’implémentation d’un tableau d’affichage, voir [Implementing a Display Table](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

