---
title: Propriété canonique PidTagProfileServerVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d41a536-81ff-733c-2fd7-460798e057c8
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 84ff229e9914ec9074d61023873279b110fb606a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286565"
---
# <a name="pidtagprofileserverversion-canonical-property"></a>Propriété canonique PidTagProfileServerVersion

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie les informations relatives à la version de Microsoft Exchange Server à laquelle les comptes d'un profil Microsoft Outlook sont connectés.
  
## 

|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROFILE_SERVER_VERSION  <br/> |
|Identificateur :  <br/> |0x661B  <br/> |
|Type de propriété:  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Configuration du profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Un profil peut spécifier un ou plusieurs comptes qui se connectent à un serveur Exchange, mais ils doivent être connectés au même serveur Exchange.
  
Les versions d'Outlook antérieures à Microsoft Office Outlook 2007 peuvent écrire dans cette propriété pour stocker des informations sur la version d'Exchange Server à laquelle le profil actif est connecté. Toutefois, le format des informations de version varie en fonction des différentes versions d'Exchange Server. Par exemple, Outlook stocke dans **PR_PROFILE_SERVER_VERSION** la valeur décimale 6944 pour représenter uniquement le numéro de build principal dans l'identificateur de version de **6.5.6944.3** pour Microsoft Exchange Server 2003. Pour une connexion Exchange 2007, Outlook stocke le numéro de version principale et le numéro de build principal dans une représentation hexadécimale concaténée de ces nombres dans la propriété. Un identificateur de version d'Exchange 2007 de **8.0.685.24** a une version majeure numéro 8 et un numéro de build majeur 685 en décimal. La conversion des deux numéros en notation hexadécimale vous permet d'obtenir les éléments 0x8 et 0x2AD. En concaténant ces deux nombres, Outlook stocke la valeur 0x82AD dans **PR_PROFILE_SERVER_VERSION** en représentation hexadécimale. 
  
Outlook 2007 ne lit pas ou n'écrit pas cette propriété. Il prend en charge **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**. 
  
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

