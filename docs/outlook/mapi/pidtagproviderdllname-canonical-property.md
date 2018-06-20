---
title: Propriété canonique PidTagProviderDllName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderDllName
api_type:
- COM
ms.assetid: 9ddb38eb-9a32-4dbe-b42c-6ea9db98acd2
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d75f22af3f8c9184da55ec57e08cf4db832ed174
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786457"
---
# <a name="pidtagproviderdllname-canonical-property"></a>Propriété canonique PidTagProviderDllName

  
  
**S’applique à**: Outlook 
  
Contient le nom de fichier de base de la bibliothèque de liens dynamiques fournisseur MAPI service (DLL).
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W  <br/> |
|Identificateur :  <br/> |0x300A  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Zone :  <br/> |MAPI courantes  <br/> |
   
## <a name="remarks"></a>Remarques

MAPI utilise une convention d’affectation de noms de fichier DLL. Nom de base contient les caractères jusqu'à six identifient de manière unique la DLL. MAPI ajoute la chaîne 32 sur le nom DLL de base pour identifier la version qui s’exécute sur les plateformes 32 bits. Par exemple, lorsque le nom MAPI. DLL est spécifié, MAPI construit le nom du fichier MAPI32. DLL pour représenter la version 32 bits correspondante de la DLL.
  
Ces propriétés doivent spécifier le nom de base. MAPI ajoute la chaîne 32 comme il convient. Dans le cadre de cette propriété entraîne une erreur, y compris la chaîne 32.
  
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

