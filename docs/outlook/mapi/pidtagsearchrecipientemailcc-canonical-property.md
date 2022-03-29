---
title: Propriété canonique PidTagSearchRecipientEmailCc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 38fe217d-cf2e-51de-c97a-acb015129fd3
description: Contient une chaîne Unicode en cours d’interrogation dans les adresses de messagerie ou affiche les noms des destinataires adressés dans la ligne Cc des messages.
ms.openlocfilehash: f5bc6cb8e5cc5ac9feb5efedd6268441d06c80af
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64456377"
---
# <a name="pidtagsearchrecipientemailcc-canonical-property"></a>Propriété canonique PidTagSearchRecipientEmailCc

**S’applique à** : Outlook 2013 | Outlook 2016
  
Contient une chaîne Unicode en cours d’interrogation dans la liste des adresses de messagerie ou affiche les noms des destinataires adressés dans la ligne **Cc** des messages de la banque.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SEARCH_RECIP_EMAIL_CC_W  <br/> |
|Identificateur :  <br/> |0x0EA7  <br/> |
|Type de propriété :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Recherche  <br/> |

## <a name="related-resources"></a>Ressources connexes

> [!NOTE]
> Cette balise de restriction MAPI, utilisée lorsque vous recherchez des adresses e-mail ou des noms complets pour lesquels le message est envoyé en tant que copie carbone, peut ne pas être définie dans le fichier d’en-tête téléchargeable dont vous disposez actuellement. Vous pouvez l’ajouter à votre code à l’aide de la valeur suivante : `#define PR_SEARCH_RECIP_EMAIL_CC_W PROP_TAG(PT_UNICODE, 0x0EA7)`
  
### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Microsoft Exchange Server de protocole.

[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations de manipulation d’une configuration de liste de dossiers de recherche.

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
