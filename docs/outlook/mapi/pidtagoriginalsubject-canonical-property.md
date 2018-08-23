---
title: Propriété canonique PidTagOriginalSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSubject
api_type:
- COM
ms.assetid: 8668ba4f-3236-4a87-a5aa-9cf7eea3d87b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: b49398b822e6972a8a6d02e1dff9c2316ce6eb33
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566634"
---
# <a name="pidtagoriginalsubject-canonical-property"></a>Propriété canonique PidTagOriginalSubject

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient l’objet du message d’origine pour une utilisation dans un rapport sur le message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W  <br/> |
|Identificateur :  <br/> |0x0049  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont initialement définies pour la même valeur que la propriété **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).
  
Les propriétés de l’objet sont généralement petites chaînes de moins de 256 caractères, et un fournisseur de magasin de message n’est pas tenu prendre en charge l’interface Object Linking and Embedding (OLE) **IStream** sur eux. Le client doit toujours tentent d’accéder par le biais de l’interface **IMAPIProp** tout d’abord et recourir aux **IStream** que si **MAPI_E_NOT_ENOUGH_MEMORY** est renvoyé. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère la synchronisation des données de l’objet messagerie entre un serveur et un client.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.
    
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

