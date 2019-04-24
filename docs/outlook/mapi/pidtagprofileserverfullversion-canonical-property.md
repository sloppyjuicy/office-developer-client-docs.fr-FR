---
title: Propriété canonique PidTagProfileServerFullVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9456178e9426d7a5fe17382d876f507daa0251f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341600"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a>Propriété canonique PidTagProfileServerFullVersion

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie la version complète et les informations de création relatives au serveur Microsoft Exchange auquel les comptes d'un profil sont connectés.
  
## 

|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROFILE_SERVER_FULL_VERSION  <br/> |
|Identificateur :  <br/> |0x663B  <br/> |
|Type de propriété:  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Configuration du profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Un profil peut spécifier un ou plusieurs comptes qui se connectent à un serveur Exchange, mais ils doivent être connectés au même serveur Exchange.
  
Les versions d'Outlook antérieures à Microsoft Office Outlook 2007 ne prennent pas en charge cette propriété. Pour ces versions d'Outlook, vérifiez l'existence de **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** dans le profil. 
  
En règle générale, si la boîte aux lettres active est connectée à un serveur Exchange, Outlook 2007 stocke les informations de version d'Exchange Server dans la propriété **PR_PROFILE_SERVER_FULL_VERSION** du profil actif. Outlook stocke les informations dans une structure **EXCHANGE_STORE_VERSION_NUM** qui contient les numéros de version principale et secondaire, ainsi que les numéros de build principaux et secondaires. Par exemple, pour stocker l'identificateur de version d'Exchange Server **8.0.685.24**, le numéro de version majeure est 8 et le numéro de version mineure est 0 et le numéro de build majeur est 685 et le numéro de build mineur est 24.
  
Seul un des **PR_PROFILE_SERVER_VERSION** ou **PR_PROFILE_SERVER_FULL_VERSION** est susceptible d'exister dans un profil, mais il n'existe aucune garantie qui existe toujours dans un profil. Outlook ne peut pas écrire dans l'une ou l'autre des propriétés tant qu'il n'a pas réussi à se connecter au serveur Exchange. 
  
Dans le modèle objet Outlook, vous pouvez utiliser la propriété **ExchangeMailboxServerVersion** de l'objet **namespace** pour rechercher la version d'Exchange Server sur laquelle la boîte aux lettres active est hébergée. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés.
    
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

