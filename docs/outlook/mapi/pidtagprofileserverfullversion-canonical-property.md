---
title: Propriété canonique PidTagProfileServerFullVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 66c6b8d50947baafb726c41c28e3bb4d675eab4f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616417"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a>Propriété canonique PidTagProfileServerFullVersion

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie la version complète et les informations de build sur les Microsoft Exchange Server à laquelle les comptes d’un profil sont connectés.
  
## 

|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROFILE_SERVER_FULL_VERSION  <br/> |
|Identificateur :  <br/> |0x663B  <br/> |
|Type de propriété :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Configuration de profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Un profil peut spécifier un ou plusieurs comptes qui se connectent à un Exchange Server, mais ils doivent être connectés au même Exchange Server.
  
Les versions Outlook antérieures à Microsoft Office Outlook 2007 ne la prise en charge. Pour ces versions de Outlook, vérifiez l’existence de PR_PROFILE_SERVER_VERSION **[dans](pidtagprofileserverversion-canonical-property.md)** le profil. 
  
En règle générale, si la boîte aux lettres active est connectée à un Exchange Server, Outlook 2007 stocke toutes les informations de version Exchange Server dans la propriété **PR_PROFILE_SERVER_FULL_VERSION** dans le profil actif. Outlook stocke les informations dans une structure **EXCHANGE_STORE_VERSION_NUM** qui contient les numéros de version principaux et mineurs, ainsi que les numéros de build principaux et mineurs. Par exemple, pour stocker l’identificateur de version Exchange Server de **8.0.685.24,** le numéro de version principal est 8 et le numéro de version mineure est 0, et le numéro de build principal est 685 et le numéro de build mineure est 24.
  
Une seule **des** PR_PROFILE_SERVER_VERSION ou **PR_PROFILE_SERVER_FULL_VERSION** est susceptible d’exister dans un profil, mais il n’existe aucune garantie qu’il existe toujours dans un profil. Outlook n’écrit dans aucune des propriétés tant qu’elle ne s’est pas connectée au Exchange Server. 
  
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

