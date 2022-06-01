---
title: Propriété canonique PidTagAlternateRecipient
description: Décrit la propriété canonique PidTagAlternateRecipient, qui contient une liste d’identificateurs d’entrée pour d’autres destinataires.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAlternateRecipient
api_type:
- HeaderDef
ms.assetid: df787b60-2f53-42ac-89b5-1b52c906f472
ms.openlocfilehash: c408ba849ad752f9787db5b456fa2b8bc271b905
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815988"
---
# <a name="pidtagalternaterecipient-canonical-property"></a>Propriété canonique PidTagAlternateRecipient

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une liste d’identificateurs d’entrée pour les destinataires de remplacement désignés par le destinataire d’origine. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ALTERNATE_RECIPIENT  <br/> |
|Identificateur :  <br/> |0x3A01  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Adresse  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée pour les messages transférés automatiquement. Il contient une structure [FLATENTRYLIST](flatentrylist.md) de destinataires alternatifs. Si le transfert automatique n’est pas autorisé ou si aucun autre destinataire n’a été désigné, un rapport non remis est généré. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère la commande et le flux des transferts de données entre un client et un serveur.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Convertit entre les objets IETF RFC2445, RFC2446 et RFC2447, ainsi que les objets de rendez-vous et de réunion.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Encode et décode les objets de message et de pièce jointe dans une représentation de flux efficace.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que propriétés associées.
    
Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[FLATENTRYLIST](flatentrylist.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

