---
title: Propriété canonique PidLidSideEffects
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSideEffects
api_type:
- COM
ms.assetid: 90d601d9-5eeb-40b6-885d-ccd8a95ae322
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2d57e6a195036ead9eb42666876e91a72f65eb8b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385696"
---
# <a name="pidlidsideeffects-canonical-property"></a>Propriété canonique PidLidSideEffects

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Détermine comment un objet message est géré par le client agissant sur l’entrée de l’utilisateur final.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidSideEffects  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID de type long (capot) :  <br/> |0x00008510  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Configuration d’exécution  <br/> |
   
## <a name="remarks"></a>Remarques

Doit être définie à une opération de bits ou zéro ou plusieurs des indicateurs suivants.
  
|**Nom**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|seOpenToDelete  <br/> |0x0001  <br/> |Un traitement supplémentaire est requis sur l’objet de message lors de la suppression.  <br/> |
|seNoFrame  <br/> |0x0008  <br/> |Aucune interface utilisateur n’est associé à l’objet du message.  <br/> |
|seCoerceToInbox  <br/> |0x0010  <br/> |Un traitement supplémentaire est requis sur l’objet de message lorsque le déplacement ou la copie à un objet folder dont la propriété **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) « erreur. Remarque ».  <br/> |
|seOpenTocopy  <br/> |0 x 0020  <br/> |Un traitement supplémentaire est requis sur l’objet de message lors de la copie dans un autre dossier.  <br/> |
|seOpenToMove  <br/> |0x0040  <br/> |Un traitement supplémentaire est requis sur l’objet de message lors du déplacement vers un autre dossier.  <br/> |
|seOpenForCtxMenu  <br/> |0 x 0100  <br/> |Un traitement supplémentaire est requis sur l’objet de message lors de l’affichage des verbes à l’utilisateur final.  <br/> |
|seCannotUndoDelete  <br/> |0 x 0400  <br/> |Ne peut pas annuler l’opération de suppression, ne doit pas être définie sauf si la valeur est « seOpenToDelete ».  <br/> |
|seCannotUndoCopy  <br/> |0 x 0800  <br/> |Ne peut pas annuler l’opération de copie, ne doit pas être définie sauf si la valeur est « seOpenTocopy ».  <br/> |
|seCannotUndoMove  <br/> |0 x 1000  <br/> |Ne peut pas annuler l’opération de déplacement, ne doit pas être définie sauf si la valeur est « seOpenToMove ».  <br/> |
|seHasScript  <br/> |0 x 2000  <br/> |L’objet du message contient un script de l’utilisateur final.  <br/> |
|seOpenToPermDelete  <br/> |0 x 4000  <br/> |Un traitement supplémentaire est nécessaire pour supprimer définitivement l’objet du message.  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit une définition de propriété et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

