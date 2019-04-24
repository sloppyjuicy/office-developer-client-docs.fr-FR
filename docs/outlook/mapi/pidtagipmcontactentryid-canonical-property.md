---
title: Propriété canonique PidTagIpmContactEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmContactEntryId
api_type:
- HeaderDef
ms.assetid: fccbbb15-dd08-4310-83d7-bf57eb3ed5de
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8f0c79fa098b8bca0518921a25d88a229e23e955
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327901"
---
# <a name="pidtagipmcontactentryid-canonical-property"></a>Propriété canonique PidTagIpmContactEntryId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l' **ID** d'entrée du dossier de contacts Outlook. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IPM_CONTACT_ENTRYID  <br/> |
|Identificateur :  <br/> |0x36D1  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est stockée dans le dossier boîte de réception et dans le dossier racine de la Banque de messages. Pour accéder à la propriété sur une banque de messages spécifique, procédez comme suit: 
  
1. Tout d'abord, recherchez la propriété dans le dossier boîte de réception. Utilisez **IMsgStore:: GetReceiveFolder** pour obtenir une référence à la propriété **EntryID** du dossier boîte de réception. 
    
2. Si **IMsgStore:: GetReceiveFolder** réussit, utilisez la référence à la propriété **EntryID** de la boîte de réception et **IMsgStore:: OpenEntry** pour ouvrir la boîte de réception et obtenir une référence à un objet **IMAPIFolder** . 
    
3. Si **IMsgStore:: OpenEntry** réussit, utilisez la référence renvoyée à l'objet **IMAPIFolder** et **IMAPIProp:: GetProps** pour obtenir la propriété souhaitée. 
    
4. En cas d'échec de l'étape 1, 2 ou 3, recherchez la propriété dans le dossier racine. Pour ce faire, utilisez **IMsgStore:: OpenEntry**, en spécifiant null pour * * lpEntryID * *, pour ouvrir le dossier racine de la Banque de messages et obtenir une référence à l'objet **IMAPIFolder** . 
    
5. Si l'ouverture du dossier racine réussit, utilisez la référence renvoyée à l'objet **IMAPIFolder** et **IMAPIProp:: GetProps** pour obtenir la propriété souhaitée. 
    
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations de création et de localisation des dossiers spéciaux dans une boîte aux lettres.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Spécifie les méthodes de connexion et de configuration des boîtes aux lettres en tant que délégués, ainsi que les interactions avec les objets message et Calendar lorsqu'ils agissent pour le compte d'un autre utilisateur.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

