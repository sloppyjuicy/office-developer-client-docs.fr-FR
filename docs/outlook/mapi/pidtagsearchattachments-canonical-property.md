---
title: Propriété canonique PidTagSearchAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 534c3881-e12f-f228-7760-788fe2b72ae8
description: Contient une chaîne Unicode en cours d’interrogation dans le contenu des pièces jointes de la banque Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: ba34f8f1eeceaf5946f2fdacbfcaa994d085ec1e
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63783433"
---
# <a name="pidtagsearchattachments-canonical-property"></a>Propriété canonique PidTagSearchAttachments

**S’applique à** : Outlook 2013 | Outlook 2016
  
Contient une chaîne Unicode en cours d’interrogation dans le contenu des pièces jointes de la banque.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SEARCH_ATTACHMENTS_W  <br/> |
|Identificateur :  <br/> |0x0EA5  <br/> |
|Type de propriété :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Recherche  <br/> |

## <a name="related-resources"></a>Ressources connexes

> [!NOTE]
> Cette balise de restriction MAPI, utilisée lorsque vous recherchez le contenu des pièces jointes, peut ne pas être définie dans le fichier d’en-tête téléchargeable dont vous disposez actuellement. Vous pouvez l’ajouter à votre code à l’aide de la valeur suivante : `#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`
  
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
