---
title: Propriété canonique PidTagBodyHtml
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagBodyHtml
api_type:
- HeaderDef
ms.assetid: 93b9215a-5900-411c-a0ae-6bba62cd5a1e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ece1ec0de9b619615bbbd77c2c3a3851b6e92476
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579179"
---
# <a name="pidtagbodyhtml-canonical-property"></a>Propriété canonique PidTagBodyHtml

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la version HTML (Hypertext Markup Language) du texte du message. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W  <br/> |
|Identificateur :  <br/> |0x1013  <br/> |
|Type de données :  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés contiennent le même texte de message que **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), mais en HTML. 
  
Une magasin de messages qui prend en charge le code HTML indique cela en STORE_HTML_OK l’indicateur **PR_STORE_SUPPORT_MASK** **(** [PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)). 
  
 **Notez** **STORE_HTML_OK** n’est pas défini dans les versions de Mapidefs.h incluses avec Microsoft® Exchange Server 2000 et versions antérieures. Si **STORE_HTML_OK** n’est pas définie, utilisez la valeur 0x00010000 à la place. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et pièce jointe.
    
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

