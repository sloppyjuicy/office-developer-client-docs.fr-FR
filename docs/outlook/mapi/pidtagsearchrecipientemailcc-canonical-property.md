---
title: Propriété canonique PidTagSearchRecipientEmailCc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 38fe217d-cf2e-51de-c97a-acb015129fd3
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 03501e14740d7b27bd54d761ae701e8863ad79dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358946"
---
# <a name="pidtagsearchrecipientemailcc-canonical-property"></a>Propriété canonique PidTagSearchRecipientEmailCc

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une chaîne Unicode interrogée dans la liste des adresses de messagerie ou des noms d'affichage des destinataires qui sont traités dans la ligne **CC** des messages de la Banque. 
  
## 

|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SEARCH_RECIP_EMAIL_CC_W  <br/> |
|Identificateur :  <br/> |0x0EA7  <br/> |
|Type de propriété:  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Rechercher  <br/> |
   
## <a name="related-resources"></a>Ressources associées

> [!NOTE]
> Cette balise de restriction MAPI, utilisée lorsque vous recherchez des adresses de messagerie ou des noms d'affichage auxquels le message est envoyé en tant que copie carbone, ne peut pas être définie dans le fichier d'en-tête téléchargeable dont vous disposez actuellement. Vous pouvez l'ajouter à votre code à l'aide de la valeur suivante: >`#define PR_SEARCH_RECIP_EMAIL_CC_W PROP_TAG(PT_UNICODE, 0x0EA7)`
  
### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Microsoft Exchange Server connexes.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour la manipulation d'une configuration de liste des dossiers de recherche.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés qui sont répertoriées en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

