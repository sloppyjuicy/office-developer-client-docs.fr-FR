---
title: Propriété canonique PidTagAdditionalRenEntryIdsEx
description: Décrit la propriété canonique PidTagAdditionalRenEntryIdsEx, qui contient des ID d’entrée de dossier spéciaux pour un objet store.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAdditionalRenEntryIdsEx
api_type:
- HeaderDef
ms.assetid: b5e896e7-c0c6-4ad1-bf91-9daba3a1e4d4
ms.openlocfilehash: 273343acc40c258eea3efde7dc83756ffe4922b4
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816009"
---
# <a name="pidtagadditionalrenentryidsex-canonical-property"></a>Propriété canonique PidTagAdditionalRenEntryIdsEx

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des ID d’entrée de dossier spéciaux pour un objet store. Chaque entrée de cette propriété à valeurs multiples peut être mappée à un ou plusieurs ID d’entrée, c’est-à-dire qu’il existe une relation un-à-plusieurs entre une entrée et ses ID d’entrée associés.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ADDITIONAL_REN_ENTRYIDS_EX  <br/> |
|Identificateur :  <br/> |0x36D9  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |application Outlook  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété est utilisée, elle contient un tableau de blocs qui spécifie les ID d’entrée pour les dossiers. Les blocs suivent le format spécifié par les quatre tableaux suivants.
  
**Bloc PersistData**

|**Name**|**Type (Type)**|**Size**|**Description**|
|:-----|:-----|:-----|:-----|
|**PersistID** <br/> |WORD  <br/> |2  <br/> |Valeur d’identificateur de type pour cette entrée **PersistData** . Consultez la table « Valeurs PersistBlockType » pour obtenir la liste des valeurs valides. |
|**DataElementsSize** <br/> |WORD  <br/> |2  <br/> |Taille, en octets, du champ **DataElements** . |
|**DataElements** <br/> |tableau de blocs **PersistElement**  <br/> |variable  <br/> |Indique le nombre d’entrées **PersistElement** pour le magasin. Consultez la table « Bloc PersistElement » pour connaître le format de cette structure. |
   
**Valeurs PersistBlockType**

|**Name**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|PERSIST_SENTINEL  <br/> |0x0000  <br/> |Indique qu’aucun bloc **PersistData** ne sera traité. |
|RSF_PID_RSS_SUBSCRIPTION  <br/> |0x8001  <br/> |Indique que ce bloc contient des données pour le dossier Abonnements RSS. |
|RSF_PID_SEND_AND_TRACK  <br/> |0x8002  <br/> |Indique que ce bloc contient des données pour le dossier De traitement du courrier suivi. |
|RSF_PID_TODO_SEARCH  <br/> |0x8004  <br/> |Indique que ce bloc contient des données pour le dossier de recherche To-Do. |
|RSF_PID_CONV_ACTIONS  <br/> |0x8006  <br/> |Indique que ce bloc contient des données pour le dossier Conversation Action Paramètres. |
|RSF_PID_COMBINED_ACTIONS  <br/> |0x8007  <br/> |Cette valeur est réservée. |
|RSF_PID_SUGGESTED_CONTACTS  <br/> |0x8008  <br/> |Indique que ce bloc contient des données pour le dossier Contacts suggérés. |
|RSF_PID_CONTACT_SEARCH  <br/> |0x8009  <br/> |Indique que ce bloc contient des données pour le dossier Recherche de contacts. Utilisé uniquement par Outlook. |
|RSF_PID_BUDDYLIST_PDLS  <br/> |0x800A  <br/> |Indique que ce bloc contient des données pour le dossier Listes de contacts de messagerie instantanée. Le dossier référencé contient des listes de distribution personnelles (PDL) représentant chaque groupe dans la liste de contacts par messagerie instantanée. Utilisé par Outlook et Exchange. |
|RSF_PID_BUDDYLIST_CONTACTS  <br/> |0x800B  <br/> |Indique que ce bloc contient des données pour le dossier Contacts par messagerie instantanée. Le dossier référencé contient les contacts individuels référencés par les groupes de listes de contacts par messagerie instantanée. Utilisé par Outlook et Exchange. |
   
Si la valeur **PersistBlockType** n’est pas l’une des valeurs définies ici, le bloc **PersistData** est ignoré et le traitement se poursuit jusqu’à ce qu’un PERSIST_SENTINEL **PersistID** soit traité ou que la fin du flux soit atteinte. 
  
**PersistElementBlock**

|**Name**|**Type (Type)**|**Size**|**Description**|
|:-----|:-----|:-----|:-----|
|**ElementID** <br/> |WORD  <br/> |2  <br/> |Spécifie la valeur de l’identificateur de type pour ce bloc **PersistElement** . Consultez la table « Valeurs PersistElementType » pour obtenir la liste des valeurs valides. |
|**ElementDataSize** <br/> |WORD  <br/> |2  <br/> |Spécifie la taille, en octets, du champ **ElementData** . |
|**ElementData** <br/> |tableau de données binaires  <br/> |variable  <br/> |Contient les données de cette paire **PersistID** + **ElementID** . |
   
**Valeurs PersistElementType**

|**Name**|**Valeur**|**Valeur d’ElementDataSize**|**Description**|
|:-----|:-----|:-----|:-----|
|RSF_ELID_HEADER  <br/> |0x0002  <br/> |0x0004  <br/> |Indique que le champ **ElementData** de ce bloc contient une valeur d’en-tête DWORD. L’interprétation de cette valeur dépend du type **PersistID** du bloc. Pour tous les types **PersistID** spécifiés dans [[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb.aspx), cette valeur est égale à zéro. |
|RSF_ELID_ENTRYID  <br/> |0x0001  <br/> |variable  <br/> |Indique que ce bloc contient **l’EntryID** du dossier spécifié par **PersistID**. |
|ELEMENT_SENTINEL  <br/> |0x0000  <br/> |0x0000  <br/> |Indique qu’aucun bloc **PersistElement** ne sera traité. |
   
Si la valeur **PersistElementType** n’est pas l’une des valeurs définies ici, le bloc **PersistElement** est ignoré et le traitement se poursuit jusqu’à ce qu’une ELEMENT_SENTINEL **ElementID** soit traitée ou que la fin du flux soit atteinte. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permet la gestion des listes d’autorisation/de blocage et la détermination des courriers indésirables.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations de création et de localisation des dossiers spéciaux dans une boîte aux lettres.
    
[[MS-OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> Identifie et marque les messages électroniques conçus pour inciter les destinataires à divulguer des informations sensibles (telles que des mots de passe et d’autres informations personnelles) à une source non fiable.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que propriétés associées.
    
Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

