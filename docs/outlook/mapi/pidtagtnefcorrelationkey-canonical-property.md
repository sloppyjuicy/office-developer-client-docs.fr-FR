---
title: Propriété canonique PidTagTnefCorrelationKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagTnefCorrelationKey
api_type:
- COM
ms.assetid: a7f05c8c-59b4-4d5b-8e70-ebcde5f2ed45
description: Contient une valeur qui met en corrélation une pièce jointe TNEF (Transport Neutral Encapsulation Format) avec un message.
ms.openlocfilehash: 0995f8b012a0d5f40858c67994a6ddb72812857a
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64454578"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a>Propriété canonique PidTagTnefCorrelationKey

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur qui met en corrélation une pièce jointe TNEF (Transport Neutral Encapsulation Format) avec un message.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_TNEF_CORRELATION_KEY  <br/> |
|Identificateur :  <br/> |0x007F  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Il est recommandé que les sous-objets de pièce jointe TNEF exposent cette propriété. Cette propriété détermine si un fichier TNEF entrant appartient au message à qui il est joint. Il est principalement utilisé par les fournisseurs de transport et les passerelles.
  
Sur un message sortant, le fournisseur de transport doit calculer une valeur binaire propre à ce message, ou utiliser une valeur existante qui répond à l’exigence d’unicité, telle qu’un identificateur de message. Le fournisseur de transport doit stocker cette valeur dans cette propriété, puis appeler la méthode [ITnef::AddProps](itnef-addprops.md) pour l’encapsuler. La même valeur doit également être stockée dans l’enveloppe de transport à un endroit défini par le fournisseur, tel que l’en-tête du message. 
  
Sur un message entrant, le fournisseur de transport doit appeler la méthode [ITnef::ExtractProps](itnef-extractprops.md) pour décaler la pièce jointe TNEF, puis comparer cette propriété à la valeur stockée dans l’enveloppe de transport. Si les valeurs correspondent, le TNEF doit être traitée normalement, c’est-à-dire que toutes les propriétés extraites de la pièce jointe TNEF doivent être utilisées. Si les valeurs ne correspondent pas, toutes les propriétés de la pièce jointe TNEF doivent être ignorées. Si cette propriété n’est pas définie, le fichier TNEF doit être considéré comme appartenant à ce message et les autres propriétés extraites de celui-ci doivent être utilisées. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère l’ordre et le flux des transferts de données entre un client et un serveur.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet en objets de message.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Code et décode les objets de message et de pièce jointe dans une représentation de flux efficace.
    
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

