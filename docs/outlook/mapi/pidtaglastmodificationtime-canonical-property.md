---
title: Propriété canonique PidTagLastModificationTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLastModificationTime
api_type:
- HeaderDef
ms.assetid: a64e5300-6865-4588-8e1b-158cfd9c60c2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dea709b457e28efef62718fc388621e01c4eb5bf
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387327"
---
# <a name="pidtaglastmodificationtime-canonical-property"></a>Propriété canonique PidTagLastModificationTime

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la date et l’heure de dernière modification de l’objet ou le sous-objet. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_LAST_MODIFICATION_TIME  <br/> |
|Identificateur :  <br/> |0x3008  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Heure du message  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est initialement définie sur la même valeur que la propriété **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md)). Pièce jointe sous-objets peuvent mettre à jour selon les besoins en copiant l’heure de dernière modification mis à jour par le système de fichiers natif. Une application cliente peut définir cette propriété qu’au premier appel à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Ensuite le fournisseur doit mettre à jour **PR_LAST_MODIFICATION_TIME** pendant chaque appel **IMAPIProp::SaveChanges** . 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère la synchronisation des données de l’objet messagerie entre un serveur et un client.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.
    
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

