---
title: Propriété canonique PidTagRemindersOnlineEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRemindersOnlineEntryId
api_type:
- COM
ms.assetid: cad25cca-248d-4845-9d60-7aa60f2dda62
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4c1468b5052c20a4d33e338347016461811852e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563391"
---
# <a name="pidtagremindersonlineentryid-canonical-property"></a>Propriété canonique PidTagRemindersOnlineEntryId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient **l’EntryID** du dossier de rappels. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_REM_ONLINE_ENTRYID  <br/> |
|Identificateur :  <br/> |0x36D5  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Conteneur MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est stockée dans le dossier Boîte de réception et dans le dossier racine de la boutique de messages. Pour accéder à la propriété sur une magasin de messages spécifique, faites ce qui suit. 
  
1. Tout d’abord, recherchez la propriété dans le dossier Boîte de réception. Utilisez [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) pour obtenir une référence à **EntryID** pour le dossier Boîte de réception. 
    
2. Si **IMsgStore::GetReceiveFolder** réussit, utilisez la référence à **EntryID** de la boîte de réception et [de l’IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir la boîte de réception et obtenir une référence à un objet **IMAPIFolder.** 
    
3. Si **IMsgStore::OpenEntry** réussit, utilisez la référence renvoyée à l’objet **IMAPIFolder** et [à IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la propriété souhaitée. 
    
4. Si l’étape 1, 2 ou 3 échoue, recherchez la propriété dans le dossier racine. Pour ce faire, utilisez **IMsgStore::OpenEntry**, en spécifiant NULL pour **lpEntryID,** pour ouvrir le dossier racine de la magasin de messages et obtenir une référence à l’objet **IMAPIFolder.** 
    
5. Si l’ouverture du dossier racine réussit, utilisez la référence renvoyée à l’objet **IMAPIFolder** et **à IMAPIProp::GetProps** pour obtenir la propriété souhaitée. 
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations permettant de créer et de localiser les dossiers spéciaux dans une boîte aux lettres.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

