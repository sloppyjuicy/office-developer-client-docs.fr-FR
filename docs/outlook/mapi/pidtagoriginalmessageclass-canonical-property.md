---
title: Propriété canonique PidTagOriginalMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagOriginalMessageClass
api_type:
- COM
ms.assetid: 49deb153-03c6-4be2-a3a5-53cca01accba
description: Contient la classe du message d’origine à utiliser dans un rapport pour Outlook 2013 et Outlook 2016.
ms.openlocfilehash: 609fde1cd865eb8af4377bd16dd395708bdb4c37
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64523633"
---
# <a name="pidtagoriginalmessageclass-canonical-property"></a>Propriété canonique PidTagOriginalMessageClass

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la classe du message d’origine à utiliser dans un rapport.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIG_MESSAGE_CLASS, PR_ORIG_MESSAGE_CLASS_A, PR_ORIG_MESSAGE_CLASS_W  <br/> |
|Identificateur :  <br/> |0x004B  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Propriétés de messagerie sécurisée  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés contiennent une copie **PR_MESSAGE_CLASS (**[PidTagMessageClass](pidtagmessageclass-canonical-property.md)) du message pour lequel l’état est généré.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Code et décode les objets de message et de pièce jointe dans une représentation de flux efficace.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

