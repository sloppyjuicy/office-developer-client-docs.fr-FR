---
title: Propriété canonique PidTagServiceDllName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDllName
api_type:
- COM
ms.assetid: a651af84-1711-449e-ba7e-5ce09cafa02b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: d2917f2119fde38686397b65956113bc430b2e31
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570813"
---
# <a name="pidtagservicedllname-canonical-property"></a>Propriété canonique PidTagServiceDllName

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient le nom de fichier de la DLL contenant la fonction de point d’entrée de message service fournisseur à appeler pour la configuration.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W  <br/> |
|Identificateur :  <br/> |0x3D0A  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque le nom de la fonction point d’entrée apparaît dans la méthode **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)), il indique que le point d’entrée existe.
  
MAPI utilise une convention d’affectation de noms de fichier DLL. Nom de base contient les caractères jusqu'à six identifient de manière unique la DLL. MAPI ajoute la chaîne 32 sur le nom DLL de base pour identifier la version qui s’exécute sur les plateformes 32 bits. Par exemple, lorsque le nom MAPI. DLL est spécifié, MAPI construit le nom du fichier MAPI32. DLL pour représenter la version 32 bits correspondante de la DLL.
  
Ces propriétés doivent spécifier le nom de base. MAPI ajoute la chaîne 32 comme il convient. Dans le cadre du résultat de ces propriétés dans une erreur, y compris la chaîne 32.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

