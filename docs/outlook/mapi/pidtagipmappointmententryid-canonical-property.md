---
title: Propriété canonique PidTagIpmAppointmentEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmAppointmentEntryId
api_type:
- HeaderDef
ms.assetid: a6e8c8fb-b76a-4a73-b112-6399e4d94233
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d27506edf6eb40f6b244733336b8b381ea941442
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384758"
---
# <a name="pidtagipmappointmententryid-canonical-property"></a>Propriété canonique PidTagIpmAppointmentEntryId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient **propriété EntryID** du dossier calendrier Outlook. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IPM_APPOINTMENT_ENTRYID  <br/> |
|Identificateur :  <br/> |0x36D0  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est stockée dans le dossier boîte de réception et dans le dossier racine de la banque de messages. Pour accéder à la propriété sur une banque de messages spécifique, procédez comme suit. 
  
1. Tout d’abord, recherchez la propriété dans le dossier boîte de réception. Utilisez [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) pour obtenir une référence à **propriété EntryID** du dossier boîte de réception. 
    
2. Si **IMsgStore::GetReceiveFolder** se déroule correctement, puis utilisez la référence à **propriété EntryID** de la boîte de réception et [IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir la boîte de réception et d’obtenir une référence à un objet **IMAPIFolder** . 
    
3. Si **IMsgStore::OpenEntry** se déroule correctement, puis utilisez la référence renvoyée à l’objet **IMAPIFolder** et [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la propriété souhaitée. 
    
4. En cas d’échec de l’étape 1, 2 ou 3, recherchez la propriété dans le dossier racine. Pour cela, utilisez **IMsgStore::OpenEntry**, spécifiant la valeur NULL pour **lpEntryID**, pour ouvrir le dossier racine de la banque de messages et d’obtenir une référence à l’objet **IMAPIFolder** . 
    
5. Si le dossier racine est réussi, puis utilisez la référence renvoyée à l’objet **IMAPIFolder** et **IMAPIProp::GetProps** pour obtenir la propriété souhaitée. 
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
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

