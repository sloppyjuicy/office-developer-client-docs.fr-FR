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
ms.openlocfilehash: 571ac25d6bc738f8289e3019c342820682d08c28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786439"
---
# <a name="pidtagprofileserverversion-canonical-property"></a>Propriété canonique PidTagProfileServerVersion

  
  
**S’applique à**: Outlook 
  
Spécifie des informations sur la version de Microsoft Exchange Server à laquelle les comptes dans un profil Microsoft Outlook sont connectés.
  
## 

|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PROFILE_SERVER_VERSION  <br/> |
|Identificateur :  <br/> |0x661B  <br/> |
|Type de propriété :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Configuration d’un profil MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Un profil peut spécifier un ou plusieurs comptes qui se connectent à un serveur Exchange, mais ils doivent être connectés au même serveur Exchange.
  
Versions d’Outlook antérieures à Microsoft Office Outlook 2007 peuvent écrire dans cette propriété pour stocker les informations relatives à la version d’Exchange Server auquel le profil actif est connecté. Toutefois, le format des informations de version varie pour différentes versions d’Exchange Server. Par exemple, les banques Outlook dans **PR_PROFILE_SERVER_VERSION** la valeur décimale 6944 pour représenter uniquement la version principale numéro de build dans l’identificateur de version de **6.5.6944.3** pour Microsoft Exchange Server 2003. Pour une connexion à Exchange 2007, Outlook stocke le numéro de version principale et la version principale numéro de version dans une représentation hexadécimale concaténée de ces numéros dans la propriété. Un identificateur de version d’Exchange 2007 de **8.0.685.24** possède un numéro de version majeur 8 et un numéro de version majeur 685 en décimal. Conversion de deux nombres en hexadécimal, vous obtenez 0 x 8 et 0x2AD. Concaténation de ces deux nombres, Outlook stocke la valeur 0x82AD dans **PR_PROFILE_SERVER_VERSION** en représentation hexadécimale. 
  
Outlook 2007 ne pas lire ou écrire cette propriété. Il prend en charge **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**. 
  
Seul **PR_PROFILE_SERVER_VERSION** ou **PR_PROFILE_SERVER_FULL_VERSION** est susceptible d’exister dans un profil, mais il n’existe aucune garantie que soit toujours existe dans un profil. Outlook n’écrit pas dans des propriétés jusqu'à ce qu’il s’est connecté au serveur Exchange. 
  
Dans le modèle objet Outlook, vous pouvez utiliser la propriété **ExchangeMailboxServerVersion** de l’objet **NameSpace** pour trouver la version du serveur Exchange qui héberge la boîte aux lettres active. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés.
    
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

