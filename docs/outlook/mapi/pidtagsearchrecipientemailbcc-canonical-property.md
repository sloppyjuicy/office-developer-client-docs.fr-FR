---
title: Propriété canonique PidTagSearchRecipientEmailBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d9561d13-8d52-500c-5369-15a2cf5c92c3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5b0db4b3bc7903aae74fa7275d3e27e22d628514
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359156"
---
# <a name="pidtagsearchrecipientemailbcc-canonical-property"></a>Propriété canonique PidTagSearchRecipientEmailBcc

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une chaîne Unicode en cours d’interrogation dans la liste des adresses de messagerie ou affiche les noms des destinataires adressés dans la ligne **BcC** des messages non envoyés dans la banque. 
  
## 

|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SEARCH_RECIP_EMAIL_BCC_W  <br/> |
|Identificateur :  <br/> |0x0EA8  <br/> |
|Type de propriété :  <br/> |PT_UNICODE  <br/> |
|Accès :  <br/> |Recherche  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est uniquement pertinente pour les messages de la boutique qui n’ont pas été envoyés, car les messages qui ont été envoyés ou reçus ne contiennent pas d’informations bcc.
  
> [!NOTE]
> Cette balise de restriction MAPI, utilisée lors de la recherche d’adresses de messagerie ou de noms complets vers lesquels le message sera envoyé en tant que copie carbone non voyante, peut ne pas être définie dans le fichier d’en-tête téléchargeable dont vous disposez actuellement. Vous pouvez l’ajouter à votre code en utilisant la valeur suivante : >  `#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Microsoft Exchange Server protocole.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations de manipulation d’une configuration de liste de dossiers de recherche.
    
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

