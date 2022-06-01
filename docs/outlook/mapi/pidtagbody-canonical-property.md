---
title: PidTagBody Canonical, propriété
description: Décrit la propriété canonique PidTagBody, qui contient le texte du message et s’applique à Outlook 2013 et Outlook 2016.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagBody
api_type:
- HeaderDef
ms.assetid: 47c0d0fe-4d57-4b81-bdb5-336de85c194c
ms.openlocfilehash: 5d5f2fbc60d4eed18267f28fdb897d7d31fbae9b
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815981"
---
# <a name="pidtagbody-canonical-property"></a>PidTagBody Canonical, propriété

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le texte du message.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_BODY, PR_BODY_A, PR_BODY_W  <br/> |
|Identificateur :  <br/> |0x1000  <br/> |
|Type de données :  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont généralement utilisées uniquement dans un message interpersonnel (IPM). 
  
Les magasins de messages qui prennent en charge le format de texte enrichi ignorent les modifications apportées aux espaces blancs dans le texte du message. Lorsque **PR_BODY** est stocké pour la première fois, le magasin de messages génère et stocke également la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), la version RTF du texte du message. Si la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) est appelée par la suite et **PR_BODY** a été modifiée, le magasin de messages appelle la fonction [RTFSync](rtfsync.md) pour garantir la synchronisation avec la version RTF. Si seul l’espace blanc a été modifié, les propriétés restent inchangées. Cela préserve toute mise en forme RTF nontrivial lorsque le message transite par des clients et des systèmes de messagerie non compatibles RTF. 
  
La valeur de cette propriété doit être exprimée dans la page de codes du système d’exploitation sur lequel MAPI s’exécute. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

