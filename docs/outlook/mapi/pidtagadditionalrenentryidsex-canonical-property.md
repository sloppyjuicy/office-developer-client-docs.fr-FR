---
title: Propriété canonique PidTagAdditionalRenEntryIdsEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAdditionalRenEntryIdsEx
api_type:
- HeaderDef
ms.assetid: b5e896e7-c0c6-4ad1-bf91-9daba3a1e4d4
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d3a8dc45bb131f5d2e7ff370617a10e3096a99f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785677"
---
# <a name="pidtagadditionalrenentryidsex-canonical-property"></a>Propriété canonique PidTagAdditionalRenEntryIdsEx

  
  
**S’applique à**: Outlook 
  
Contient l’identificateur d’entrée de dossier spécial pour un objet store. Chaque entrée de cette propriété à valeurs multiples peut être mappée à un ou plusieurs identificateurs d’entrée, autrement dit, il existe une relation un-à-plusieurs entre une entrée et son identificateur d’entrée associé.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ADDITIONAL_REN_ENTRYIDS_EX  <br/> |
|Identificateur :  <br/> |0x36D9  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Application Outlook  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété est utilisée, il contient un tableau de blocs qui spécifie l’identificateur d’entrée pour les dossiers. Les blocs de suivent le format spécifié par les quatre tableaux suivants.
  
**Bloc PersistData**

|**Name**|**Type**|**Size**|**Description**|
|:-----|:-----|:-----|:-----|
|**PersistID** <br/> |WORD  <br/> |2  <br/> |Tapez la valeur de l’identificateur de cette entrée **PersistData** . Voir le tableau des « Valeurs PersistBlockType » pour la liste des valeurs valides.  <br/> |
|**DataElementsSize** <br/> |WORD  <br/> |2  <br/> |Taille, en octets, du champ **DataElements** .  <br/> |
|**DataElements** <br/> |tableau des blocs de **PersistElement**  <br/> |variable  <br/> |Indique le nombre d’entrées **PersistElement** existe pour le magasin. Consultez le tableau « PersistElement Block » pour le format de cette structure.  <br/> |
   
**Valeurs PersistBlockType**

|**Nom**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|PERSIST_SENTINEL  <br/> |0x0000  <br/> |Indique qu’aucune blocs **PersistData** supplémentaires ne seront traitées.  <br/> |
|RSF_PID_RSS_SUBSCRIPTION  <br/> |0 x 8001  <br/> |Indique que ce bloc contient des données pour le dossier Abonnements RSS.  <br/> |
|RSF_PID_SEND_AND_TRACK  <br/> |0x8002  <br/> |Indique que ce bloc contient des données pour le dossier de suivi de messagerie traitement.  <br/> |
|RSF_PID_TODO_SEARCH  <br/> |0 x 8004  <br/> |Indique que ce bloc contient des données pour le dossier de recherche des tâches.  <br/> |
|RSF_PID_CONV_ACTIONS  <br/> |0x8006  <br/> |Indique que ce bloc contient des données pour le dossier Paramètres d’Action de Conversation.  <br/> |
|RSF_PID_COMBINED_ACTIONS  <br/> |0x8007  <br/> |Cette valeur est réservée.  <br/> |
|RSF_PID_SUGGESTED_CONTACTS  <br/> |0x8008  <br/> |Indique que ce bloc contient des données pour le dossier Contacts suggérés.  <br/> |
|RSF_PID_CONTACT_SEARCH  <br/> |0x8009  <br/> |Indique que ce bloc contient des données pour le dossier de recherche de Contacts.  <br/> Utilisé uniquement par Outlook.  <br/> |
|RSF_PID_BUDDYLIST_PDLS  <br/> |0x800A  <br/> |Indique que ce bloc contient des données pour le dossier listes des contacts de messagerie instantanée (IM). Le dossier référencé contient des listes de Distribution personnelles (PDLs) représentant chaque groupe au sein de la liste des contacts de messagerie instantanée.  <br/> Utilisé par Outlook et Exchange.  <br/> |
|RSF_PID_BUDDYLIST_CONTACTS  <br/> |0x800B  <br/> |Indique que ce bloc contient des données pour le dossier Contacts de messagerie instantanée. Le dossier référencé contient les contacts référencés par les groupes de la liste des contacts de messagerie instantanée.  <br/> Utilisé par Outlook et Exchange.  <br/> |
   
Si la valeur **PersistBlockType** n’est pas une de celles définies ici, le bloc **PersistData** est ignoré et le traitement se poursuit jusqu'à ce que la fin du flux de données ou une PERSIST_SENTINEL **PersistID** est traitée. 
  
**PersistElementBlock**

|**Name**|**Type**|**Size**|**Description**|
|:-----|:-----|:-----|:-----|
|**ElementID** <br/> |WORD  <br/> |2  <br/> |Spécifie la valeur d’identificateur de type de ce bloc **PersistElement** . Voir le tableau des « Valeurs PersistElementType » pour obtenir la liste des valeurs valides.  <br/> |
|**ElementDataSize** <br/> |WORD  <br/> |2  <br/> |Spécifie la taille, en octets, du champ **ElementData** .  <br/> |
|**ElementData** <br/> |tableau de données binaires  <br/> |variable  <br/> |Contient les données pour cette **PersistID** + **ElementID** paire.  <br/> |
   
**Valeurs PersistElementType**

|**Nom**|**Valeur**|**Valeur de ElementDataSize**|**Description**|
|:-----|:-----|:-----|:-----|
|RSF_ELID_HEADER  <br/> |0x0002  <br/> |0x0004  <br/> |Indique que le champ de **ElementData** du bloc contient une valeur DWORD en-tête. Comment cette valeur est interprétée dépend du type de **PersistID** du bloc.  <br/> Pour tous les types de **PersistID** spécifiés dans [[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb.aspx), cette valeur est égale à zéro.  <br/> |
|RSF_ELID_ENTRYID  <br/> |0x0001  <br/> |variable  <br/> |Indique que ce bloc contienne **propriété EntryID** du dossier spécifié par **PersistID**.  <br/> |
|ELEMENT_SENTINEL  <br/> |0x0000  <br/> |0x0000  <br/> |Indique qu’aucune blocs **PersistElement** supplémentaires ne seront traitées.  <br/> |
   
Si la valeur **PersistElementType** n’est pas une de celles définies ici, le bloc **PersistElement** est ignoré et le traitement se poursuit jusqu'à ce que la fin du flux de données ou une ELEMENT_SENTINEL **ElementID** est traité. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permet la gestion des listes autoriser/bloquer et la détermination des messages de courrier indésirable.
    
[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour la création et la localisation des dossiers spéciaux dans une boîte aux lettres.
    
[[MS-OXPHISH]](http://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> Identifie et marque les messages électroniques qui sont conçues pour amener les destinataires à dévoiler des informations sensibles (comme les mots de passe et autres informations personnelles) à une source non fiable.
    
### <a name="header-files"></a>Fichiers d’en-tête

MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Vue d'ensemble de la propri�t� MAPI](mapi-property-overview.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

