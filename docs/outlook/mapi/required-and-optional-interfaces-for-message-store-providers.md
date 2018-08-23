---
title: Interfaces obligatoires et facultatives pour les fournisseurs de banque de messages
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc62e57e-82a4-4f37-8d1b-7cdf828b951e
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: 3305aaadbcf7d53b801ddaf7e31a0d63145fc7ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586962"
---
# <a name="required-and-optional-interfaces-for-message-store-providers"></a>Interfaces obligatoires et facultatives pour les fournisseurs de banque de messages

 
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
MAPI définit un ensemble d’interfaces qui sont associées aux fournisseurs de magasins de message. En raison de la grande variété de fonctionnalités qu’une banque de messages peut choisir d’implémenter, certains de ces interfaces sont obligatoires, mais pas. Le tableau suivant répertorie les interfaces MAPI qui sont liées aux fournisseurs de magasins de message, indique si les interfaces sont obligatoires ou facultatives et décrit leur fonction.
  
|**Interface**|**Status**|**Description**|
|:-----|:-----|:-----|
|[IMSProvider](imsprovideriunknown.md) <br/> |Obligatoire  <br/> |Journaux sur ou sur une banque de messages.  <br/> |
|[IMSLogon](imslogoniunknown.md) <br/> |Obligatoire  <br/> |Ouvre les dossiers ou les messages, vérifie l’identité de la banque de messages et gère les notifications.  <br/> |
|[IMsgStore](imsgstoreimapiprop.md) <br/> |Obligatoire  <br/> |Ouvre les dossiers ou les messages, recherche les dossiers spéciaux et gère les envois de messages.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Obligatoire  <br/> |Rechercher et manipuler des messages et les sous-dossiers.  <br/> |
|[IMessage](imessageimapiprop.md) <br/> |Obligatoire  <br/> |Gère les pièces jointes et définit certaines propriétés d’un message.  <br/> |
|[IMAPITable](imapitableiunknown.md) <br/> |Obligatoire  <br/> |Permet aux autres objets de présenter des collections de données pour les différents composants MAPI.  <br/> |
|[IMAPIStatus](imapistatusimapiprop.md) <br/> |Obligatoire  <br/> |Permet aux clients de valider l’état d’une banque de messages et d’effectuer certaines tâches de configuration.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Facultatif  <br/> |Accède à des propriétés de pièce jointe du message si le fournisseur de banque prend en charge les pièces jointes.  <br/> |
|**IStorage** <br/> |Facultatif  <br/> |Gère les objets de stockage structuré si le fournisseur de banque prend en charge les pièces jointes objet OLE.  <br/> |
|**IStream** <br/> |Facultatif  <br/> |Permet aux objets de message et des pièces jointes lire et écrire des données dans des objets stream.  <br/> |
|**IStreamDocfile** <br/> |Facultatif  <br/> |Permet d’ouvrir un objet de stockage, tel qu’un fichier au format de fichier OLE 2.0 composé certains fournisseurs de services.  <br/> |
   
Les informations de base que vous devez implémenter **IMAPIFolder**, **IMessage**, **IMAPIStatus**et **IMAPITable** sont documentées dans les rubriques de référence pour ces interfaces. Cette section contient des informations supplémentaires plus directement liées à un fournisseur de magasin de message. Le reste des interfaces MAPI doit être implémenté selon les informations de cette section et dans les rubriques de référence appropriée. Consultez la section COM et ActiveX Object Services dans le SDK de Windows pour plus d’informations sur l’implémentation de **IStorage** **IStream**et **IStreamDocFile**.
  
## <a name="see-also"></a>Voir aussi



[D�veloppement d'un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)

