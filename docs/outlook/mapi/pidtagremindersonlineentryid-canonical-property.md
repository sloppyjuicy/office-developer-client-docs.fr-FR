---
title: Propriété canonique PidTagRemindersOnlineEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemindersOnlineEntryId
api_type:
- COM
ms.assetid: cad25cca-248d-4845-9d60-7aa60f2dda62
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b3d1d2a20720bd1c4b15464cd24aac4415721ae8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563176"
---
# <a name="pidtagremindersonlineentryid-canonical-property"></a>Propriété canonique PidTagRemindersOnlineEntryId

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient **propriété EntryID** du dossier rappels. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_REM_ONLINE_ENTRYID  <br/> |
|Identificateur :  <br/> |0x36D5  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Conteneur MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est stockée dans le dossier boîte de réception et dans le dossier racine de la banque de messages. Pour accéder à la propriété sur une banque de messages spécifique, procédez comme suit. 
  
1. Tout d’abord, recherchez la propriété dans le dossier boîte de réception. Utilisez [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) pour obtenir une référence à **propriété EntryID** du dossier boîte de réception. 
    
2. Si **IMsgStore::GetReceiveFolder** se déroule correctement, puis utilisez la référence à **propriété EntryID** de la boîte de réception et [IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir la boîte de réception et d’obtenir une référence à un objet **IMAPIFolder** . 
    
3. Si **IMsgStore::OpenEntry** se déroule correctement, puis utilisez la référence renvoyée à l’objet **IMAPIFolder** et [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la propriété souhaitée. 
    
4. En cas d’échec de l’étape 1, 2 ou 3, recherchez la propriété dans le dossier racine. Pour cela, utilisez **IMsgStore::OpenEntry**, spécifiant la valeur NULL pour **lpEntryID**, pour ouvrir le dossier racine de la banque de messages et d’obtenir une référence à l’objet **IMAPIFolder** . 
    
5. Si le dossier racine est réussi, puis utilisez la référence renvoyée à l’objet **IMAPIFolder** et **IMAPIProp::GetProps** pour obtenir la propriété souhaitée. 
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour la création et la localisation des dossiers spéciaux dans une boîte aux lettres.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

