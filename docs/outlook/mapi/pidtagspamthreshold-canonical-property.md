---
title: Propriété canonique PidTagSpamThreshold
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2b2d6b8e-e3dd-4a9b-8bb5-53add675605d
description: Valeur longue qui indique le niveau de filtrage du courrier indésirable pour Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: 5d5ff7787359da98c443c403523497d0e30a753b
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63762255"
---
# <a name="pidtagspamthreshold-canonical-property"></a>Propriété canonique PidTagSpamThreshold

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Valeur longue qui indique le niveau de filtrage du courrier indésirable.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SPAM_THRESHOLD  <br/> |
|ID long (LID) :  <br/> | 0x041B  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Courrier indésirable  <br/> |
   
## <a name="values"></a>Values

Les valeurs pour le filtrage du courrier indésirable sont les suivantes :
  
|**Niveau de courrier indésirable**|**Valeur**|
|:-----|:-----|
|Aucune  <br/> |0xFFFFFFFF  <br/> |
|Faible  <br/> |0x00000006  <br/> |
|Moyenne  <br/> |0x00000005  <br/> |
|Élevé  <br/> |0x00000003  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Microsoft Exchange Server protocole.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permet la gestion des listes d’adresses de courriers indésirables et la détermination des messages électroniques indésirables.
    
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

