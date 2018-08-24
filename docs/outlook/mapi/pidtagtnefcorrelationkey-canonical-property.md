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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 760196668ffb3c486803f27b50ff809177e8e6f3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588614"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a>Propriété canonique PidTagTnefCorrelationKey

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient une valeur qui met en corrélation une pièce jointe TNEF Transport Neutral Encapsulation Format () avec un message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_TNEF_CORRELATION_KEY  <br/> |
|Identificateur :  <br/> |0x007F  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Enveloppe MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Il est recommandé que les sous-objets de pièce jointe TNEF exposent cette propriété. Cette propriété détermine si un fichier TNEF entrant appartient au message, à qu'il est connecté. Il est utilisé principalement par les passerelles et les fournisseurs de transport.
  
Dans un message sortant, le fournisseur de transport doit calculer une valeur binaire unique à ce message, ou utiliser une valeur existante qui satisfait les règles d’unicité, par exemple un identificateur de message. Le fournisseur de transport doit stocker cette valeur dans cette propriété, puis appelez la méthode [ITnef::AddProps](itnef-addprops.md) pour encapsuler. La même valeur doit également être stockée dans l’enveloppe de transport dans un emplacement défini par le fournisseur, telles que l’en-tête du message. 
  
Sur un message entrant, le fournisseur de transport doit appeler la méthode [ITnef::ExtractProps](itnef-extractprops.md) à décapsulent la pièce jointe TNEF et comparez cette propriété avec la valeur stockée dans l’enveloppe de transport. Si les valeurs correspondent, TNEF sera traité normalement, autrement dit, toutes les propriétés extraites de la pièce jointe TNEF doivent être utilisées. Si les valeurs ne correspondent pas, toutes les propriétés de la pièce jointe TNEF doivent être ignorées. Si cette propriété n’est pas définie, le fichier TNEF doit être considérées comme appartenant à ce message, et les autres propriétés extraites d’elle doivent être utilisées. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère l’ordre et le flux pour les transferts de données entre un client et le serveur.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet aux objets de message.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.
    
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

