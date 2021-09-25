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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a51a2c12c1c5609cf02ec4e19ed01dc4ae217328
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613393"
---
# <a name="pidtaglastmodificationtime-canonical-property"></a>Propriété canonique PidTagLastModificationTime

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la date et l’heure de la dernière modification de l’objet ou du sous-objet. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_LAST_MODIFICATION_TIME  <br/> |
|Identificateur :  <br/> |0x3008  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Heure du message  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est initialement définie sur la même valeur que la **propriété PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)). Les sous-objets de pièce jointe peuvent le mettre à jour si nécessaire en copiant l’heure de la dernière modification conservée par le système de fichiers natif. Une application cliente peut définir cette propriété jusqu’au premier appel de la [méthode IMAPIProp::SaveChanges.](imapiprop-savechanges.md) À partir de là, le fournisseur doit mettre PR_LAST_MODIFICATION_TIME jour **pendant** chaque **appel IMAPIProp::SaveChanges.** 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et pièce jointe.
    
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

