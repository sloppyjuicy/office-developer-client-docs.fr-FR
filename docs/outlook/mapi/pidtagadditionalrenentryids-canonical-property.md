---
title: Propriété canonique PidTagAdditionalRenEntryIds
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAdditionalRenEntryIds
api_type:
- HeaderDef
ms.assetid: 8c6e7ca2-1824-4cca-bf69-3c1ea52727de
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4984055d370f3f8ab617b11b2d834ba277ef105a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282360"
---
# <a name="pidtagadditionalrenentryids-canonical-property"></a>Propriété canonique PidTagAdditionalRenEntryIds

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient les identificateurs d'entrée de certains dossiers spéciaux. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ADDITIONAL_REN_ENTRYIDS  <br/> |
|Identificateur :  <br/> |0x36D8  <br/> |
|Type de données :  <br/> |PT_MV_BINARY  <br/> |
|Domaine :  <br/> |Application Outlook  <br/> |
   
## <a name="remarks"></a>Remarques

Les cinq premières entrées de cette propriété à valeurs multiples s'appliquent aux dossiers spéciaux suivants, s'ils existent dans la Banque:
  
0-dossier de conflits
  
1-dossier problèmes de synchronisation
  
2-dossier pannes locales
  
dossier de défaillances de 3 serveurs
  
4-dossier courrier indésirable
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations de création et de localisation des dossiers spéciaux dans une boîte aux lettres.
    
[[MS-OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> Identifie et marque les messages électroniques conçus pour inciter les destinataires à divulguer des informations sensibles (telles que des mots de passe et d'autres informations personnelles) à une source non fiable.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Active la gestion des listes d'autorisation/de blocage et la détermination des messages électroniques indésirables.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapitags. h
  
> Contient les définitions des propriétés indiquées en tant que propriétés associées.
    
Mapidefs. h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)


[À propos de l’API de magasin](https://msdn.microsoft.com/library/aa192884.aspx)

