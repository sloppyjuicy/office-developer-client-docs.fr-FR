---
title: Propriété canonique PidTagProfileServerVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d41a536-81ff-733c-2fd7-460798e057c8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 84ff229e9914ec9074d61023873279b110fb606a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286565"
---
# <a name="pidtagprofileserverversion-canonical-property"></a>Propriété canonique PidTagProfileServerVersion

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie des informations sur la version de Microsoft Exchange Server à laquelle les comptes d’un profil Microsoft Outlook sont connectés.
  
## 

|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROFILE_SERVER_VERSION  <br/> |
|Identificateur :  <br/> |0x661B  <br/> |
|Type de propriété :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Configuration de profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Un profil peut spécifier un ou plusieurs comptes qui se connectent à un Exchange Server, mais ils doivent être connectés au même Exchange Server.
  
Les versions d’Outlook antérieures à Microsoft Office Outlook 2007 peuvent écrire dans cette propriété pour stocker des informations sur la version de Exchange Server à laquelle le profil actif est connecté. Toutefois, le format des informations de version varie selon les versions des Exchange Server. Par exemple, Outlook stocke dans **PR_PROFILE_SERVER_VERSION** la valeur décimale 6944 pour représenter uniquement le numéro de build principal dans l’identificateur de version **6.5.6944.3** pour Microsoft Exchange Server 2003. Pour une connexion Exchange 2007, Outlook stocke le numéro de version principal et le numéro de build principal dans une représentation hexadécimale concassée de ces numéros dans la propriété. Un identificateur de version Exchange 2007 de **8.0.685.24** a un numéro de version principal 8 et un numéro de build majeur 685 en décimal. En convertissant les deux nombres en nombres hexadécimals, vous obtenez 0x8 et 0x2AD. En concassant ces deux nombres, Outlook stocke la valeur 0x82AD dans **PR_PROFILE_SERVER_VERSION** représentation hexadécimale. 
  
Outlook 2007 ne lit pas ou n’écrit pas dans cette propriété. Il prend en **[charge PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**. 
  
Une seule **des** PR_PROFILE_SERVER_VERSION ou **PR_PROFILE_SERVER_FULL_VERSION** est susceptible d’exister dans un profil, mais il n’existe aucune garantie qu’il existe toujours dans un profil. Outlook n’écrit dans aucune des propriétés tant qu’il ne s’est pas connecté au Exchange Server. 
  
Dans le modèle objet Outlook, vous pouvez utiliser la propriété **ExchangeMailboxServerVersion** de l’objet **NameSpace** pour rechercher la version de Exchange Server sur laquelle la boîte aux lettres active est hébergée. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés.
    
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

