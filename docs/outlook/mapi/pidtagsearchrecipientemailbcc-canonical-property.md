---
title: Propriété canonique PidTagSearchRecipientEmailBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d9561d13-8d52-500c-5369-15a2cf5c92c3
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 0f65c197999f23d959657cbfee9c6fbb0aaf439f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566284"
---
# <a name="pidtagsearchrecipientemailbcc-canonical-property"></a>Propriété canonique PidTagSearchRecipientEmailBcc

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient une chaîne Unicode qui est interrogée dans la liste des adresses de messagerie ou les noms complets des destinataires dans la ligne **Cci** des messages en attente sur le magasin. 
  
## 

|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SEARCH_RECIP_EMAIL_BCC_W  <br/> |
|Identificateur :  <br/> |0x0EA8  <br/> |
|Type de propriété :  <br/> |PT_UNICODE  <br/> |
|Access :  <br/> |Recherche  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est uniquement aux messages qui n’ont pas été envoyés, dans le magasin étant donné que les messages qui ont été envoyés ou reçus ne contiennent pas d’informations Cci.
  
> [!NOTE]
> Cette balise de restriction MAPI, utilisée pour rechercher des adresses de messagerie ou des noms d’affichage vers lequel le message sera envoyé en tant que copie carbone invisible, pas peut-être être définie dans le fichier d’en-tête téléchargeable dont vous disposez. Vous pouvez l’ajouter à votre code à l’aide de la valeur suivante : >`#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole connexes Microsoft Exchange Server.
    
[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour la manipulation d’une configuration de liste de dossier de recherche.
    
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

