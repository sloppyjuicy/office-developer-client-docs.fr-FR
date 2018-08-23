---
title: Propriété canonique PidTagSendInternetEncoding
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSendInternetEncoding
api_type:
- COM
ms.assetid: ae408b4f-dee3-484b-a19c-f472cfa95996
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 33b9931a269eb4b5ee0429287d60fa1962b0e4f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584232"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a>Propriété canonique PidTagSendInternetEncoding

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un masque binaire composé des préférences de codage. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SEND_INTERNET_ENCODING  <br/> |
|Identificateur :  <br/> |0x3A71  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Remarques

Définir cette propriété pour indiquer les options de codage utilisées. 
  
Cette propriété contient les indicateurs suivants :
  
BODY_ENCODING_HTML 
  
> Coder le texte du message dans le code HTML. Cet indicateur est ignoré à moins que l’indicateur ENCODING_MIME est défini. 
    
BODY_ENCODING_TEXT_AND_HTML 
  
> Coder le texte du message à l’aide de texte et HTML en tant que solutions à parties multiples Multipurpose Internet Mail Extensions (MIME). Cet indicateur est ignoré à moins que l’indicateur ENCODING_MIME est défini. 
    
ENCODING_MIME 
  
> Coder le message à l’aide de MIME. Si cet indicateur n’est pas défini, MAPI encode le texte du message en texte brut et les pièces jointes dans UUENCODE. 
    
ENCODING_PREFERENCE 
  
> Utilisez les autres indicateurs dans ce masque de bits pour déterminer le type de codage. Si cet indicateur n’est pas défini, MAPI laisse au système de messagerie pour prendre des décisions de codage. 
    
MAC_ATTACH_ENCODING_APPLEDOUBLE 
  
> Coder les pièces jointes de Macintosh en mode double Apple. Cet indicateur est ignoré à moins que l’indicateur ENCODING_MIME est défini. 
    
MAC_ATTACH_ENCODING_APPLESINGLE 
  
> Coder les pièces jointes de Macintosh en mode unique Apple. Cet indicateur est ignoré à moins que l’indicateur ENCODING_MIME est défini. 
    
MAC_ATTACH_ENCODING_UUENCODE 
  
> Coder les pièces jointes de Macintosh dans UUENCODE. Si l’indicateur ENCODING_MIME est défini, cet indicateur est ignoré et codage BinHex est utilisé à la place. 
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet aux objets de message.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

