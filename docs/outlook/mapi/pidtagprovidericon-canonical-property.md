---
title: Propriété canonique PidTagProviderIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagProviderIcon
api_type:
- COM
ms.assetid: 59c84b1f-13b5-484b-b703-2fb9fcc6c7eb
description: Contient une chaîne Unicode qui spécifie une ou plusieurs icônes personnalisées à afficher pour un fournisseur MAPI dans la barre d’état Outlook dans les états en ligne et hors connexion.
ms.openlocfilehash: 9e78640142a25925113e03584989914022897d84
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63763907"
---
# <a name="pidtagprovidericon-canonical-property"></a>Propriété canonique PidTagProviderIcon

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une chaîne Unicode qui spécifie une ou plusieurs icônes personnalisées à afficher pour un fournisseur MAPI dans la barre d’état Microsoft Office Outlook dans les états en ligne et hors connexion.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROVIDER_ICON, PR_PROVIDER_ICON_W  <br/> |
|Identificateur :  <br/> |0x3417  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Magasin de messages MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés spécifient le fichier de ressources qui contient une icône personnalisée qui représente un fournisseur MAPI dans un état en ligne, et éventuellement une autre icône personnalisée en mode hors connexion. Outlook demande toujours ces propriétés dans la représentation Unicode. 
  
Par exemple, la valeur de propriété suivante indique à Outlook de charger l’ID d’icône 1001 à partir de la mymod32.dll de module et d’utiliser cette icône pour l’état en ligne : `mymod32.dll,#1001` Étant donné qu’il n’existe aucune icône spécifique au fournisseur pour l’état hors connexion, dans ce cas, l’icône Outlook hors connexion standard est utilisée dans la barre d’état. 
  
La valeur de propriété suivante indique à Outlook de charger l’ID d’icône 1001 à partir du mymod32.dll de module et d’utiliser cette icône pour l’état en ligne, ainsi que de charger l’ID d’icône 1002 à partir de ce même module `mymod32.dll,#1001,#1002`à utiliser pour l’état hors connexion : Aucune Outlook’icône n’est utilisée dans la barre d’état. 
  
Par défaut, si aucune icône personnalisée n’est spécifiée, le fournisseur est représenté par les Outlook par défaut pour l’état en ligne et l’état hors connexion. Le fournisseur peut éventuellement spécifier un nom d’affichage à afficher en adjacent à l’icône dans la barre d’état. Pour plus d’informations, **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).
  
## <a name="related-resources"></a>Ressources connexes

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

