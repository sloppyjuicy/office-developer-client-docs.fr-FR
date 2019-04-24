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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e157fa640026d13362084b30ad73cdb66a0b35b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342671"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a>Propriété canonique PidTagSendInternetEncoding

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de masque des préférences de codage. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SEND_INTERNET_ENCODING  <br/> |
|Identificateur :  <br/> |0x3A71  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Remarques

Définissez cette propriété pour indiquer les options d'encodage utilisées. 
  
Cette propriété contient les indicateurs suivants:
  
BODY_ENCODING_HTML 
  
> Codez le texte du message au format HTML. Cet indicateur est ignoré sauf si l'indicateur ENCODING_MIME est défini. 
    
BODY_ENCODING_TEXT_AND_HTML 
  
> Codez le texte du message en utilisant du texte et du code HTML en tant que solutions multifonctions MIME (Multipurpose Internet Mail Extensions) en plusieurs parties. Cet indicateur est ignoré sauf si l'indicateur ENCODING_MIME est défini. 
    
ENCODING_MIME 
  
> Codez le message en utilisant MIME. Si cet indicateur n'est pas défini, MAPI code le texte du message en texte brut et les pièces jointes dans UUENCODE. 
    
ENCODING_PREFERENCE 
  
> Utilisez les autres indicateurs de ce masque pour déterminer le codage. Si cet indicateur n'est pas défini, MAPI le laisse au système de messagerie afin de prendre des décisions de codage. 
    
MAC_ATTACH_ENCODING_APPLEDOUBLE 
  
> Coder les pièces jointes Macintosh en mode double de Apple. Cet indicateur est ignoré sauf si l'indicateur ENCODING_MIME est défini. 
    
MAC_ATTACH_ENCODING_APPLESINGLE 
  
> Coder les pièces jointes Macintosh en mode simple Apple. Cet indicateur est ignoré sauf si l'indicateur ENCODING_MIME est défini. 
    
MAC_ATTACH_ENCODING_UUENCODE 
  
> Coder les pièces jointes Macintosh dans UUENCODE. Si l'indicateur ENCODING_MIME est défini, cet indicateur est ignoré et l'encodage BinHex est utilisé à la place. 
    
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les listes d'utilisateurs, de contacts, de groupes et de ressources.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> ConVertit des conventions de messagerie standard Internet en objets message.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et Attachment.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés indiquées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

