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
ms.openlocfilehash: 57ab68d4c53693c769a4aadf8737f57ef5e73fcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335202"
---
# <a name="pidtagadditionalrenentryidsex-canonical-property"></a>Propriété canonique PidTagAdditionalRenEntryIdsEx

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des ID d'entrée de dossier spéciaux pour un objet Store. Chaque entrée de cette propriété à valeurs multiples peut être mappée à un ou plusieurs identificateurs d'entrée, c'est-à-dire qu'il existe une relation un-à-plusieurs entre une entrée et ses ID d'entrée associés.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ADDITIONAL_REN_ENTRYIDS_EX  <br/> |
|Identificateur :  <br/> |0x36D9  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Application Outlook  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété est utilisée, elle contient un tableau de blocs qui spécifie les identificateurs d'entrée pour les dossiers. Les blocs suivent le format spécifié par les quatre tableaux suivants.
  
**Bloc PersistData**

|**Name**|**Type**|**Size**|**Description**|
|:-----|:-----|:-----|:-----|
|**PersistID** <br/> |WORD  <br/> |n°2  <br/> |Type de valeur de l'identificateur pour cette entrée **PersistData** . Consultez le tableau «valeurs PersistBlockType» pour obtenir la liste des valeurs valides.  <br/> |
|**DataElementsSize** <br/> |WORD  <br/> |n°2  <br/> |Taille, en octets, du champ **DataElements** .  <br/> |
|**DataElements** <br/> |Tableau de blocs **PersistElement**  <br/> |variable  <br/> |Indique le nombre d'entrées **PersistElement** pour la Banque. Consultez la table «bloc PersistElement» pour le format de cette structure.  <br/> |
   
**Valeurs PersistBlockType**

|**Nom**|**Value**|**Description**|
|:-----|:-----|:-----|
|PERSIST_SENTINEL  <br/> |0x0000  <br/> |Indique qu'aucun autre bloc **PersistData** ne sera traité.  <br/> |
|RSF_PID_RSS_SUBSCRIPTION  <br/> |0x8001  <br/> |Indique que ce bloc contient des données pour le dossier des abonnements RSS.  <br/> |
|RSF_PID_SEND_AND_TRACK  <br/> |0x8002  <br/> |Indique que ce bloc contient des données pour le dossier de traitement du courrier suivi.  <br/> |
|RSF_PID_TODO_SEARCH  <br/> |0x8004  <br/> |Indique que ce bloc contient des données pour le dossier de recherche de tâches.  <br/> |
|RSF_PID_CONV_ACTIONS  <br/> |0x8006  <br/> |Indique que ce bloc contient des données pour le dossier des paramètres d'action de conversation.  <br/> |
|RSF_PID_COMBINED_ACTIONS  <br/> |0x8007  <br/> |Cette valeur est réservée.  <br/> |
|RSF_PID_SUGGESTED_CONTACTS  <br/> |0x8008  <br/> |Indique que ce bloc contient des données pour le dossier de contacts suggéré.  <br/> |
|RSF_PID_CONTACT_SEARCH  <br/> |0x8009  <br/> |Indique que ce bloc contient des données pour le dossier de recherche contacts.  <br/> Utilisé uniquement par Outlook.  <br/> |
|RSF_PID_BUDDYLIST_PDLS  <br/> |0x800A  <br/> |Indique que ce bloc contient des données pour le dossier listes de contacts de messagerie instantanée. Le dossier référencé contient des listes de distribution personnelles (PDLs) représentant chaque groupe dans la liste des contacts de messagerie instantanée.  <br/> Utilisé par Outlook et Exchange.  <br/> |
|RSF_PID_BUDDYLIST_CONTACTS  <br/> |0x800B  <br/> |Indique que ce bloc contient des données pour le dossier de contacts de messagerie instantanée. Le dossier référencé contient les contacts individuels référencés par les groupes de listes de contacts de messagerie instantanée.  <br/> Utilisé par Outlook et Exchange.  <br/> |
   
Si la valeur **PersistBlockType** n'est pas l'une des valeurs définies ici, le bloc **PersistData** est ignoré et le traitement se poursuit jusqu'à ce qu'une **PersistId** PERSIST_SENTINEL soit traitée ou que la fin du flux soit atteinte. 
  
**PersistElementBlock**

|**Name**|**Type**|**Size**|**Description**|
|:-----|:-----|:-----|:-----|
|**ElementID** <br/> |WORD  <br/> |n°2  <br/> |Spécifie la valeur de l'identificateur de type pour ce bloc **PersistElement** . Consultez le tableau «valeurs PersistElementType» pour obtenir la liste des valeurs valides.  <br/> |
|**ElementDataSize** <br/> |WORD  <br/> |n°2  <br/> |Spécifie la taille, en octets, du champ **ElementData** .  <br/> |
|**ElementData** <br/> |Tableau de données binaires  <br/> |variable  <br/> |Contient les données de cette paire d'**ElementID** **PersistId** + .  <br/> |
   
**Valeurs PersistElementType**

|**Nom**|**Valeur**|**Valeur de ElementDataSize**|**Description**|
|:-----|:-----|:-----|:-----|
|RSF_ELID_HEADER  <br/> |0x0002  <br/> |0x0004  <br/> |Indique que le champ **ElementData** de ce bloc contient une valeur d'en-tête DWORD. Le mode d'interprétation de cette valeur dépend du type **PersistId** du bloc.  <br/> Pour tous les types **PersistId** spécifiés dans [[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb.aspx), cette valeur est égale à zéro.  <br/> |
|RSF_ELID_ENTRYID  <br/> |0x0001  <br/> |variable  <br/> |Indique que ce bloc contient l' **EntryID** du dossier spécifié par **PersistId**.  <br/> |
|ELEMENT_SENTINEL  <br/> |0x0000  <br/> |0x0000  <br/> |Indique qu'aucun autre bloc **PersistElement** ne sera traité.  <br/> |
   
Si la valeur **PersistElementType** n'est pas l'une des valeurs définies ici, le bloc **PersistElement** est ignoré et le traitement se poursuit jusqu'à ce qu'un **ElementID** ELEMENT_SENTINEL soit traité ou que la fin du flux soit atteinte. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Active la gestion des listes d'autorisation/de blocage et la détermination des messages électroniques indésirables.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations de création et de localisation des dossiers spéciaux dans une boîte aux lettres.
    
[[MS-OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> Identifie et marque les messages électroniques conçus pour inciter les destinataires à divulguer des informations sensibles (telles que des mots de passe et d'autres informations personnelles) à une source non fiable.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapitags. h
  
> Contient les définitions des propriétés indiquées en tant que propriétés associées.
    
Mapidefs. h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

