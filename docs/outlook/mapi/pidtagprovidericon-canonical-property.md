---
title: Propriété canonique PidTagProviderIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderIcon
api_type:
- COM
ms.assetid: 59c84b1f-13b5-484b-b703-2fb9fcc6c7eb
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 55e6c8fb013e544ae04740aeaeb23ac23949cffb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286459"
---
# <a name="pidtagprovidericon-canonical-property"></a>Propriété canonique PidTagProviderIcon

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une chaîne Unicode qui spécifie une icône personnalisée ou des icônes à afficher pour un fournisseur MAPI dans la barre d'état Microsoft Office Outlook dans les États en ligne et hors connexion.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROVIDER_ICON, PR_PROVIDER_ICON_W  <br/> |
|Identificateur :  <br/> |0x3417  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Banque de messages MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés spécifient le fichier de ressources qui contient une icône personnalisée qui représente un fournisseur MAPI dans un État en ligne et, éventuellement, une autre icône personnalisée dans l'état hors connexion. Outlook demande toujours ces propriétés dans la représentation Unicode. 
  
Par exemple, la valeur de la propriété suivante demande à Outlook de charger l'ID d'icône 1001 à partir du module mymod32. dll et d'utiliser cette `mymod32.dll,#1001`icône pour l'État en ligne:. Étant donné qu'il n'existe pas d'icône spécifique au fournisseur pour l'état hors connexion, dans ce cas, l'icône Outlook hors connexion standard est utilisée dans la barre d'État. 
  
La valeur de la propriété suivante indique à Outlook de charger l'ID d'icône 1001 à partir du module mymod32. dll et d'utiliser cette icône pour l'État en ligne et de charger également l'ID d'icône 1002 à partir de ce `mymod32.dll,#1001,#1002`même module pour être utilisé pour l'état hors connexion:. Aucune icône Outlook n'est utilisée dans la barre d'État. 
  
Par défaut, si aucune icône personnalisée n'est spécifiée, le fournisseur est représenté par les icônes Outlook par défaut pour l'État en ligne et l'état hors connexion. Le fournisseur peut éventuellement spécifier un nom complet à afficher en regard de l'icône dans la barre d'État. Pour plus d'informations, voir **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).
  
## <a name="related-resources"></a>Ressources associées

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

