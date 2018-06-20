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
ms.openlocfilehash: e63d661ab8c7e410d6a0dd786819cc189813017e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785668"
---
# <a name="pidtagadditionalrenentryids-canonical-property"></a>Propriété canonique PidTagAdditionalRenEntryIds

  
  
**S’applique à**: Outlook 
  
Contient les identificateurs d’entrée de certains dossiers spéciaux. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ADDITIONAL_REN_ENTRYIDS  <br/> |
|Identificateur :  <br/> |0x36D8  <br/> |
|Type de données :  <br/> |PT_MV_BINARY  <br/> |
|Zone :  <br/> |Application Outlook  <br/> |
   
## <a name="remarks"></a>Remarques

Les cinq premières entrées de cette propriété à valeurs multiples s’appliquent aux dossiers spéciaux suivants, s’ils existent dans le magasin :
  
0 - dossier conflits
  
-1 dossier problèmes de synchronisation
  
2 - dossier défaillances local
  
3 - dossier des échecs serveur
  
4 - dossier courrier indésirable
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour la création et la localisation des dossiers spéciaux dans une boîte aux lettres.
    
[[MS-OXPHISH]](http://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> Identifie et marque les messages électroniques qui sont conçues pour amener les destinataires à dévoiler des informations sensibles (comme les mots de passe et autres informations personnelles) à une source non fiable.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permet la gestion des listes autoriser/bloquer et la détermination des messages de courrier indésirable.
    
### <a name="header-files"></a>Fichiers d’en-tête

MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)


[À propos de l’API du magasin](http://msdn.microsoft.com/en-us/library/aa192884.aspx)

