---
title: Propriété canonique PidTagLastModificationTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagLastModificationTime
api_type:
- HeaderDef
ms.assetid: a64e5300-6865-4588-8e1b-158cfd9c60c2
description: 'Contient la date et l’heure de la dernière modification de l’objet ou du sous-objet. Cette propriété est initialement définie sur la même valeur que la PR_CREATION_TIME propriété. '
ms.openlocfilehash: 6cb55991f44a1554c11e47e8c53aea32a22e9381
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64405159"
---
# <a name="pidtaglastmodificationtime-canonical-property"></a>Propriété canonique PidTagLastModificationTime

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la date et l’heure de la dernière modification de l’objet ou du sous-objet. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_LAST_MODIFICATION_TIME  <br/> |
|Identificateur :  <br/> |0x3008  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Heure du message  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est initialement définie sur la même valeur que la **propriété PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)). Les sous-objets de pièce jointe peuvent le mettre à jour si nécessaire en copiant l’heure de la dernière modification conservée par le système de fichiers natif. Une application cliente peut définir cette propriété jusqu’au premier appel de la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . À partir de là, le fournisseur doit mettre **PR_LAST_MODIFICATION_TIME jour pendant** chaque **appel IMAPIProp::SaveChanges** . 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère la synchronisation des données d’objet de messagerie entre un serveur et un client.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations des listes d’utilisateurs, de contacts, de groupes et de ressources.
    
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

