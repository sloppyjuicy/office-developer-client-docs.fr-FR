---
title: Propriété canonique PidTagSearchAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534c3881-e12f-f228-7760-788fe2b72ae8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 95729474db29fe21f808ec5c8f571bec4600db70
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382833"
---
# <a name="pidtagsearchattachments-canonical-property"></a>Propriété canonique PidTagSearchAttachments

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une chaîne Unicode qui est interrogée dans le contenu de pièce jointe dans le magasin.
  
## 

|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SEARCH_ATTACHMENTS_W  <br/> |
|Identificateur :  <br/> |0x0EA5  <br/> |
|Type de propriété :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Recherche  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

> [!NOTE]
> Cette balise de restriction MAPI, utilisée lorsque vous effectuez une recherche de contenu de pièce jointe, pas peut-être être définie dans le fichier d’en-tête téléchargeable dont vous disposez. Vous pouvez l’ajouter à votre code à l’aide de la valeur suivante : >`#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`
  
### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole connexes Microsoft Exchange Server.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour la manipulation d’une configuration de liste de dossier de recherche.
    
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

