---
title: Propri t canonique PidLidSideEffects
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidSideEffects
api_type:
- COM
ms.assetid: 90d601d9-5eeb-40b6-885d-ccd8a95ae322
description: Contient des indicateurs qui contrôlent la façon dont un objet message est géré par le client lors de l’intervention de l’utilisateur final.
ms.openlocfilehash: 7891ecb3867591fc7920c9fe0ea445150c59e7d8
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63763676"
---
# <a name="pidlidsideeffects-canonical-property"></a>Propri t canonique PidLidSideEffects

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contrôle la façon dont un objet de message est géré par le client lors de l’intervention de l’utilisateur final.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidSideEffects  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x00008510  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Configuration au moment de l’exécuter  <br/> |
   
## <a name="remarks"></a>Remarques

Doit être définie sur un bit ou zéro ou plusieurs des indicateurs suivants.
  
|**Name**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|seOpenToDelete  <br/> |0x0001  <br/> |Un traitement supplémentaire est requis sur l’objet message lors de la suppression. |
|seNoFrame  <br/> |0x0008  <br/> |Aucune interface utilisateur n’est associée à l’objet message. |
|seCoerceToInbox  <br/> |0x0010  <br/> |Un traitement supplémentaire est requis sur l’objet message lors du déplacement ou de la copie vers un objet de dossier avec **une propriété PR_CONTAINER_CLASS** ([PidTagContainerClass](pidtagcontainerclass-canonical-property.md)) de « IPF. Note ». |
|seOpenTocopy  <br/> |0x0020  <br/> |Un traitement supplémentaire est requis sur l’objet message lors de la copie dans un autre dossier. |
|seOpenToMove  <br/> |0x0040  <br/> |Un traitement supplémentaire est requis sur l’objet message lors du déplacement vers un autre dossier. |
|seOpenForCtxMenu  <br/> |0x0100  <br/> |Un traitement supplémentaire est requis sur l’objet message lors de l’affichage de verbes à l’utilisateur final. |
|seCannotUndoDelete  <br/> |0x0400  <br/> |Impossible d’annuler l’opération de suppression, ne doit pas être définie sauf si « seOpenToDelete » est définie. |
|seCannotUndoCopy  <br/> |0x0800  <br/> |Impossible d’annuler l’opération de copie, ne doit pas être définie sauf si « seOpenTocopy » est définie. |
|seCannotUndoMove  <br/> |0x1000  <br/> |Impossible d’annuler l’opération de déplacement, ne doit pas être définie sauf si « seOpenToMove » est définie. |
|seHasScript  <br/> |0x2000  <br/> |L’objet message contient un script d’utilisateur final. |
|seOpenToPermDelete  <br/> |0x4000  <br/> |Un traitement supplémentaire est nécessaire pour supprimer définitivement l’objet message. |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit une définition de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

