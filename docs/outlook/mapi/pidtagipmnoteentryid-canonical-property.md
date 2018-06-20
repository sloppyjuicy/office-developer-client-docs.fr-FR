---
title: Propriété canonique PidTagIpmNoteEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmNoteEntryId
api_type:
- HeaderDef
ms.assetid: c003f7b9-b0cd-4656-98fa-3466fda6832c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 1d46110585fb5075041942560b3a8bd5d0b125a8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786154"
---
# <a name="pidtagipmnoteentryid-canonical-property"></a>Propriété canonique PidTagIpmNoteEntryId

  
  
**S’applique à**: Outlook 
  
Contient **propriété EntryID** du dossier Notes Outlook. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IPM_NOTE_ENTRYID  <br/> |
|Identificateur :  <br/> |0x36D3  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est stockée dans le dossier boîte de réception, ainsi que le dossier racine de la banque de messages. Pour accéder à la propriété sur une banque de messages spécifique, procédez comme suit : 
  
1. Tout d’abord, recherchez la propriété dans le dossier boîte de réception. Utilisez [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) pour obtenir une référence à **propriété EntryID** du dossier boîte de réception. 
    
2. Si ** IMsgStore::GetReceiveFolder ** se déroule correctement, puis utilisez la référence à **propriété EntryID** de la boîte de réception et [IMsgStore::OpenEntry](imsgstore-openentry.md) pour ouvrir la boîte de réception et d’obtenir une référence à un objet **IMAPIFolder** . 
    
3. Si **IMsgStore::OpenEntry** se déroule correctement, puis utilisez la référence renvoyée à l’objet **IMAPIFolder** et [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la propriété souhaitée. 
    
4. En cas d’échec de l’étape 1, 2 ou 3, recherchez la propriété dans le dossier racine. Pour cela, utilisez **IMsgStore::OpenEntry**, spécifiant la valeur NULL pour **lpEntryID**, pour ouvrir le dossier racine de la banque de messages et d’obtenir une référence à l’objet **IMAPIFolder** . 
    
5. Si le dossier racine est réussi, puis utilisez la référence renvoyée à l’objet **IMAPIFolder** et **IMAPIProp::GetProps** pour obtenir la propriété souhaitée. 
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour la création et la localisation des dossiers spéciaux dans une boîte aux lettres.
    
[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Spécifie les méthodes pour la connexion et configurer des boîtes aux lettres en tant que les délégués et les interactions avec les objets de messagerie et de calendrier lorsqu’ils agissent au nom d’un autre utilisateur.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

