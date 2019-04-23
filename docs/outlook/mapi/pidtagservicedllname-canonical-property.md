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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: adf24bcd02d7efc303f911ee01a64325150339ce
ms.sourcegitcommit: 18f3d9462048859fe040e12136ff66f19066764b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "31980453"
---
# <a name="pidtagservicedllname-canonical-property"></a>Propriété canonique PidTagServiceDllName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom de fichier de la DLL contenant la fonction de point d'entrée du fournisseur de services de messagerie à appeler pour la configuration.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W  <br/> |
|Identificateur :  <br/> |0x3D0A  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque le nom de la fonction de point d'entrée apparaît dans la méthode **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)), cela indique que le point d'entrée existe.
  
MAPI utilise une convention d'affectation de noms de fichiers DLL. Il ajoute la chaîne 32 au nom de la DLL de base pour identifier la version qui s'exécute sur les plateformes 32 bits. Par exemple, lorsque le nom MAPI. DLL est spécifié, MAPI construit le nom MAPI32. DLL pour représenter la version 32 bits correspondante de la DLL.
  
Ces propriétés doivent spécifier le nom de base. MAPI ajoute la chaîne 32 comme il convient. L'inclusion de la chaîne 32 dans le cadre de ces propriétés génère une erreur.
  
## <a name="related-resources"></a>Ressources associées

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

