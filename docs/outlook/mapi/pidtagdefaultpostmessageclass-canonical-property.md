---
title: Propriété canonique PidTagDefaultPostMessageClass
description: Décrit la propriété canonique PidTagDefaultPostMessageClass, qui contient le nom d’une classe Message de formulaire personnalisé.
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
ms.openlocfilehash: 49e4249a75f14a69635a376342e13b4f640f154f
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770102"
---
# <a name="pidtagdefaultpostmessageclass-canonical-property"></a>Propriété canonique PidTagDefaultPostMessageClass

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom d’une classe message de formulaire personnalisé.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DEF_POST_MSGCLASS  <br/> |
|Identificateur :  <br/> |0x36E5  <br/> |
|Type de données :  <br/> |PT_STRING8  <br/> |
|Domaine :  <br/> |Conteneur MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété est définie sur un dossier, la valeur doit contenir exactement la classe de message de base (par exemple, « IPM. Contact » pour un dossier de contacts ou « IPM. Rendez-vous » pour un dossier de calendrier), ou commencez par la classe de message de base (par exemple, « IPM. Contact.MyContact »).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

