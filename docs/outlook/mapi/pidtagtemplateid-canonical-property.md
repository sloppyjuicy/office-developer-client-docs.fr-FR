---
title: Propriété canonique PidTagTemplateid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagTemplateid
api_type:
- COM
ms.assetid: 1a418c76-ebc7-47f2-ac91-797162e6e099
description: Contient le PR_ENTRYID, exprimé sous la forme d’un format d’ID d’entrée permanent. Cette valeur doit être présente pour tous les objets de carnet d’adresses sur un serveur NSPI.
ms.openlocfilehash: 3af96c4770d81720f495824f822e19fd2e799526
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63763494"
---
# <a name="pidtagtemplateid-canonical-property"></a>Propriété canonique PidTagTemplateid

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), exprimé sous forme de format d’ID d’entrée permanent.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_TEMPLATEID  <br/> |
|Identificateur :  <br/> |0x3902  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Carnet d'adresses MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette valeur doit être présente pour tous les objets de carnet d’adresses sur un serveur NSPI (Name Service Provider Interface), son nom unique (DN) doit correspondre à la valeur de **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) et son nom unique doit respecter la spécification de format DN spécifique au type d’objet. 
  
Cette propriété n’est pas présente sur les objets d’un carnet d’adresses en mode hors connexion.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations des listes d’utilisateurs, de contacts, de groupes et de ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

