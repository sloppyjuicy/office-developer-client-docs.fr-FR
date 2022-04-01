---
title: Propriété canonique PidTagProviderDllName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagProviderDllName
api_type:
- COM
ms.assetid: 9ddb38eb-9a32-4dbe-b42c-6ea9db98acd2
description: Contient le nom de fichier de base de la bibliothèque de liens dynamiques (DLL) du fournisseur de services MAPI. Ces propriétés doivent spécifier le nom de base.
ms.openlocfilehash: 0d74b8795c5a8d6fd561a164d60eed7a9cecd8f8
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64521859"
---
# <a name="pidtagproviderdllname-canonical-property"></a>Propriété canonique PidTagProviderDllName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom de fichier de base de la bibliothèque de liens dynamiques (DLL) du fournisseur de services MAPI.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W  <br/> |
|Identificateur :  <br/> |0x300A  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |MAPI courant  <br/> |
   
## <a name="remarks"></a>Remarques

MAPI utilise une convention d’attribution de noms de fichiers DLL. Il a ajouté la chaîne 32 au nom de la DLL de base pour identifier la version qui s’exécute sur les plateformes 32 bits. Par exemple, lorsque le nom MAPI.DLL est spécifié, MAPI construit le nom MAPI32.DLL pour représenter la version 32 bits correspondante de la DLL.
  
Ces propriétés doivent spécifier le nom de base. MAPI a ajouté la chaîne 32 selon le cas. L’utilisation de la chaîne 32 dans le cadre de cette propriété entraîne une erreur.
  
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

