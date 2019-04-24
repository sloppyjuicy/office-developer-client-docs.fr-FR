---
title: Propriété canonique PidTagTnefCorrelationKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTnefCorrelationKey
api_type:
- COM
ms.assetid: a7f05c8c-59b4-4d5b-8e70-ebcde5f2ed45
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e38cf93523c14d2d58c48e24a79249674298b4b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341950"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a>Propriété canonique PidTagTnefCorrelationKey

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur qui corrèle une pièce jointe au format TNEF (Transport Neutral Encapsulation Format) avec un message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_TNEF_CORRELATION_KEY  <br/> |
|Identificateur :  <br/> |0x007F  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Il est recommandé que les sous-objets de pièces jointes TNEF exposent cette propriété. Cette propriété détermine si un fichier TNEF entrant appartient au message auquel il est attaché. Il est principalement utilisé par les fournisseurs de transport et les passerelles.
  
Sur un message sortant, le fournisseur de transport doit calculer une valeur binaire propre à ce message ou utiliser une valeur existante qui répond à l'exigence d'unicité, comme un identificateur de message. Le fournisseur de transport doit stocker cette valeur dans cette propriété, puis appeler la méthode [ITnef:: AddProps](itnef-addprops.md) pour l'encapsuler. La même valeur doit également être stockée dans l'enveloppe de transport à un emplacement défini par le fournisseur, tel que l'en-tête du message. 
  
Sur un message entrant, le fournisseur de transport doit appeler la méthode [ITnef:: ExtractProps](itnef-extractprops.md) pour decapsulate la pièce jointe TNEF, puis comparer cette propriété avec la valeur stockée dans l'enveloppe de transport. Si les valeurs correspondent, TNEF doit être traité normalement, autrement dit, toutes les propriétés extraites de la pièce jointe TNEF doivent être utilisées. Si les valeurs ne correspondent pas, toutes les propriétés de la pièce jointe TNEF doivent être ignorées. Si cette propriété n'est pas définie, le fichier TNEF doit être considéré comme appartenant à ce message, et les autres propriétés extraites de celui-ci doivent être utilisées. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère l'ordre et le flux de transfert de données entre un client et un serveur.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> ConVertit des conventions de messagerie standard Internet en objets message.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Encode et décode les objets message et Attachment en une représentation de flux efficace.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

