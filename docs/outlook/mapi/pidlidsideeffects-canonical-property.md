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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2d57e6a195036ead9eb42666876e91a72f65eb8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331296"
---
# <a name="pidlidsideeffects-canonical-property"></a>Propriété canonique PidLidSideEffects

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contrôle la façon dont un objet message est géré par le client lorsqu'il agit sur l'entrée de l'utilisateur final.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidSideEffects  <br/> |
|Jeu de propriétés:  <br/> |PSETID_Common  <br/> |
|ID long (couvercle):  <br/> |0x00008510  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Configuration de l'exécution  <br/> |
   
## <a name="remarks"></a>Remarques

Doit être défini sur une valeur de bits or zéro ou plusieurs des indicateurs suivants.
  
|**Name**|**Value**|**Description**|
|:-----|:-----|:-----|
|seOpenToDelete  <br/> |0x0001  <br/> |Un traitement supplémentaire est requis sur l'objet message lors de la suppression.  <br/> |
|seNoFrame  <br/> |0x0008  <br/> |Aucune interface utilisateur n'est associée à l'objet message.  <br/> |
|seCoerceToInbox  <br/> |0x0010  <br/> |Un traitement supplémentaire est requis sur l'objet message lors du transfert ou de la copie d'un objet Folder avec une propriété **PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) de «IPF. Note».  <br/> |
|seOpenTocopy  <br/> |0x0020  <br/> |Un traitement supplémentaire est requis sur l'objet message lors de la copie dans un autre dossier.  <br/> |
|seOpenToMove  <br/> |0x0040  <br/> |Un traitement supplémentaire est requis sur l'objet message lors du passage à un autre dossier.  <br/> |
|seOpenForCtxMenu  <br/> |0x0100  <br/> |Un traitement supplémentaire est requis sur l'objet message lors de l'affichage des verbes à l'utilisateur final.  <br/> |
|seCannotUndoDelete  <br/> |0x0400  <br/> |Impossible d'annuler l'opération de suppression, elle ne doit pas être définie sauf si «seOpenToDelete» est défini.  <br/> |
|seCannotUndoCopy  <br/> |0x0800  <br/> |Impossible d'annuler l'opération de copie, ne doit pas être défini sauf si «seOpenTocopy» est défini.  <br/> |
|seCannotUndoMove  <br/> |0x1000  <br/> |Impossible d'annuler l'opération de déplacement, ne doit pas être défini sauf si «seOpenToMove» est défini.  <br/> |
|seHasScript  <br/> |0 x 2000  <br/> |L'objet message contient le script de l'utilisateur final.  <br/> |
|seOpenToPermDelete  <br/> |0x4000  <br/> |Un traitement supplémentaire est nécessaire pour supprimer définitivement l'objet message.  <br/> |
   
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit la définition des jeux de propriétés et les références aux spécifications du protocole Exchange Server associé.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et Attachment.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

