---
title: Propriété canonique PidTagProfileServerFullVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9456178e9426d7a5fe17382d876f507daa0251f4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396175"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a>Propriété canonique PidTagProfileServerFullVersion

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie les informations de version et de compilation complètes sur le serveur Microsoft Exchange auxquels sont connectés les comptes dans un profil.
  
## 

|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROFILE_SERVER_FULL_VERSION  <br/> |
|Identificateur :  <br/> |0x663B  <br/> |
|Type de propriété :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Configuration d’un profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Un profil peut spécifier un ou plusieurs comptes qui se connectent à un serveur Exchange, mais ils doivent être connectés au même serveur Exchange.
  
Versions d’Outlook antérieures à Microsoft Office Outlook 2007 ne prennent pas en charge cette propriété. Pour les versions d’Outlook, vérifiez l’existence de **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** dans le profil. 
  
En règle générale, si la boîte aux lettres actif est connecté à un serveur Exchange, Outlook 2007 stocke des informations complètes sur la version Exchange Server dans la propriété **PR_PROFILE_SERVER_FULL_VERSION** dans le profil actif. Outlook stocke les informations dans une structure **EXCHANGE_STORE_VERSION_NUM** qui contient les numéros de version principale et secondaire et les numéros de version principale et secondaire. Par exemple, pour stocker l’identificateur de version d’Exchange Server de **8.0.685.24**, le numéro de version principale est 8 et numéro de version secondaire est 0 et le numéro de version majeur est 685 et numéro de version secondaire est 24.
  
Seul **PR_PROFILE_SERVER_VERSION** ou **PR_PROFILE_SERVER_FULL_VERSION** est susceptible d’exister dans un profil, mais il n’existe aucune garantie que soit toujours existe dans un profil. Outlook n’écrit pas dans des propriétés jusqu'à ce qu’il s’est connecté au serveur Exchange. 
  
Dans le modèle objet Outlook, vous pouvez utiliser la propriété **ExchangeMailboxServerVersion** de l’objet **NameSpace** pour trouver la version du serveur Exchange qui héberge la boîte aux lettres active. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

