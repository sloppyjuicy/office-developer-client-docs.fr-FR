---
title: Propriété canonique PidTagOriginalSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSearchKey
api_type:
- COM
ms.assetid: ac5eb91d-31c9-459b-bb22-f4ccfc92d1db
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 26854b640669bbc6479ce90ba9cad18cdf4d9264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786343"
---
# <a name="pidtagoriginalsearchkey-canonical-property"></a>Propriété canonique PidTagOriginalSearchKey

  
  
**S’applique à**: Outlook 
  
Contient la clé de recherche d’origine pour une entrée copiée à partir d’un carnet d’adresses à un carnet d’adresses personnel ou autre carnet d’adresses accessible en écriture.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINAL_SEARCH_KEY  <br/> |
|Identificateur :  <br/> |0x3A14  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est une des propriétés qui contiennent des informations sur la source d’origine d’une entrée copiée.
  
Pour un rapport nonread, cette propriété contient une copie de la clé de recherche du destinataire du message d’origine pour lequel le rapport est généré. Lorsque le destinataire d’origine fait partie d’une liste de distribution, la clé de recherche de la liste de distribution est conservée pour le rapport.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.
    
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

