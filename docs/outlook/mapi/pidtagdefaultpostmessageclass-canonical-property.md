---
title: Propriété canonique PidTagDefaultPostMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDefaultPostMessageClass
api_type:
- HeaderDef
ms.assetid: 231c288f-547b-4463-9442-1499661b925e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bb813792b864fa414a9bd9b6f7160df6dbd2ae23
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583491"
---
# <a name="pidtagdefaultpostmessageclass-canonical-property"></a>Propriété canonique PidTagDefaultPostMessageClass

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom d’une classe de message de formulaire personnalisé.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DEF_POST_MSGCLASS  <br/> |
|Identificateur :  <br/> |0x36E5  <br/> |
|Type de données :  <br/> |PT_STRING8  <br/> |
|Domaine :  <br/> |Conteneur MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété est définie sur un dossier, la valeur doit contenir exactement la classe de message de base (par exemple, « IPM ». Contact » pour un dossier de contacts ou « IPM ». Rendez-vous » pour un dossier de calendrier) ou commencez par la classe de message de base (par exemple, « IPM. Contact.MyContact »).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
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

