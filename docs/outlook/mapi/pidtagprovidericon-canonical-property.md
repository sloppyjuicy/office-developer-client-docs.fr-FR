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
ms.openlocfilehash: 92407d56bd095135ac1c6c292aa4b1da4755e93c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786461"
---
# <a name="pidtagprovidericon-canonical-property"></a>Propriété canonique PidTagProviderIcon

  
  
**S’applique à**: Outlook 
  
Contient une chaîne Unicode qui spécifie une icône personnalisée ou des icônes à afficher pour un fournisseur MAPI dans la barre d’état Microsoft Office Outlook dans les États en ligne et hors connexion.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROVIDER_ICON, PR_PROVIDER_ICON_W  <br/> |
|Identificateur :  <br/> |0x3417  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Zone :  <br/> |Banque de messages MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés spécifient le fichier de ressources qui contient une icône personnalisée qui représente un fournisseur MAPI dans un état en ligne, et, éventuellement, une autre icône personnalisée à l’état en mode hors connexion. Outlook demande toujours ces propriétés dans la représentation Unicode. 
  
Par exemple, la valeur de propriété suivante indique à Outlook pour charger l’icône 1001 ID dans le module mymod32.dll et utiliser cette icône pour l’état en ligne : `mymod32.dll,#1001`. Dans la mesure où il n’existe aucune icône spécifiques au fournisseur pour l’état en mode hors connexion, dans ce cas, l’icône en mode hors connexion Outlook standard est utilisée dans la barre d’état. 
  
La valeur de propriété suivante indique à Outlook pour charger l’icône 1001 ID dans le module mymod32.dll et utiliser cette icône pour l’état en ligne et également charger l’icône 1002 ID à partir de ce même module à utiliser pour l’état en mode hors connexion : `mymod32.dll,#1001,#1002`. Aucune icône Outlook n’est utilisé dans la barre d’état. 
  
Par défaut, si aucune des icônes personnalisées ne sont spécifiés, le fournisseur est représenté par les icônes Outlook par défaut pour l’état en ligne et hors connexion. Le fournisseur peut éventuellement spécifier un nom complet à afficher adjacent à l’icône dans la barre d’état. Pour plus d’informations, voir **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

