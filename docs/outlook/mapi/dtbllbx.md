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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2bff20af2b3e9ea4e203e38ae38a8bc19074a727
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321233"
---
# <a name="dtbllbx"></a>DTBLLBX

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une liste qui sera utilisée dans une boîte de dialogue construite à partir d'une table d'affichage.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
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
  
> Masque de des indicateurs utilisé pour éliminer une barre de défilement horizontale ou verticale de la liste. Les indicateurs suivants peuvent être définis:
    
MAPI_NO_HBAR 
  
> Aucune barre de défilement horizontale ne doit apparaître avec la liste.
    
MAPI_NO_VBAR 
  
> Aucune barre de défilement verticale ne doit apparaître avec la liste.
    
 **ulPRSetProperty**
  
> Balise de propriété pour une propriété de n'importe quel type. Cette propriété est une des colonnes du tableau identifié par le membre **ulPRTableTable** . 
    
 **ulPRTableName**
  
> Balise de propriété pour une propriété de table de type PT_OBJECT qui peut être ouverte à l'aide d'un appel **OpenProperty** . Le nombre de colonnes que le tableau doit avoir dépend du fait que la liste soit une ou plusieurs listes de sélection. Si le membre **ulPRSetProperty** est défini sur **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), la liste autorise la sélection multiple.
    
## <a name="remarks"></a>Remarques

Une structure **DTBLLBX** décrit une liste d'un contrôle utilisé pour afficher plusieurs éléments et permettre à l'utilisateur de sélectionner un ou plusieurs des éléments. 
  
Le membre **ulPRSetProperty** et le membre **ulPRTableName** travaillent ensemble; Lorsqu'une valeur est sélectionnée dans la table, elle est réécrite dans **ulPRSetProperty** lorsque la boîte de dialogue est fermée. 
  
La valeur flags indique si une barre de défilement horizontale ou verticale doit être affichée avec la liste. Par défaut, les types de barres de défilement s'affichent si nécessaire. Les fournisseurs de services peuvent définir MAPI_NO_HBAR pour supprimer une barre de défilement horizontale et MAPI_NO_VBAR supprimer une barre de défilement verticale. 
  
Les deux membres de la balise de propriété s'emploient ensemble pour afficher les valeurs de la liste et définir les propriétés correspondantes lorsqu'un élément de la liste est sélectionné. Lorsque MAPI affiche d'abord la liste, il appelle la méthode **OpenProperty** de l'implémentation de **IMAPIProp** pour récupérer la table identifiée dans le membre **ulPRTableName** . Le nombre de colonnes dans le tableau dépend de la valeur du membre **ulPRSetProperty** . Si **ulPRSetProperty** est défini sur **PR_NULL**, la liste est une liste à sélection multiple basée sur un objet contenant des destinataires, tel qu'un conteneur de carnet d'adresses, une table de destinataires pour un message ou une table de contenu de liste de distribution. 
  
Un tableau pour une liste de sélection multiple doit inclure les colonnes suivantes:
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
 **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
  
 **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) et un maximum de cinq autres propriétés de chaîne à valeurs multiples peuvent également être affichées avec les trois colonnes obligatoires. 
  
Si le membre **ulPRSetProperty** n'est pas défini sur **PR_NULL**, la liste est une seule liste de sélection. La valeur initiale de **ulPRSetProperty** détermine la première ligne sélectionnée. Lorsqu'un utilisateur sélectionne une des lignes, le membre **ulPRSetProperty** est défini sur la valeur sélectionnée et cette valeur est réécrite dans l'implémentation de l'interface de propriété avec un appel à [IMAPIProp:: SetProps](imapiprop-setprops.md). 
  
Pour une vue d'ensemble des tables d'affichage, voir [afficher les tables](display-tables.md). Pour plus d'informations sur l'implémentation d'une table d'affichage, voir [Implementing a Display table](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

