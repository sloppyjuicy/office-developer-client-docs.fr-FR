---
title: Interfaces obligatoires et facultatives pour les fournisseurs de banques de messages
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc62e57e-82a4-4f37-8d1b-7cdf828b951e
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: 35b1d05d742b0d8defabf84b6dbf7d418ece0bbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420919"
---
# <a name="required-and-optional-interfaces-for-message-store-providers"></a>Interfaces obligatoires et facultatives pour les fournisseurs de banques de messages

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI définit un ensemble d'interfaces qui sont liées aux fournisseurs de banques de messages. En raison de la large gamme de fonctionnalités qu'un magasin de messages peut choisir d'implémenter, certaines de ces interfaces sont requises et d'autres non. Le tableau suivant répertorie les interfaces MAPI liées aux fournisseurs de banques de messages, indique si les interfaces sont obligatoires ou facultatives, et décrit leur objectif.
  
|**Interface**|**État**|**Description**|
|:-----|:-----|:-----|
|[IMSProvider](imsprovideriunknown.md) <br/> |Obligatoire  <br/> |Se connecte à une banque de messages et la désactive.  <br/> |
|[IMSLogon](imslogoniunknown.md) <br/> |Obligatoire  <br/> |Ouvre des dossiers ou des messages, vérifie l'identité de la Banque de messages et gère les notifications.  <br/> |
|[IMsgStore](imsgstoreimapiprop.md) <br/> |Obligatoire  <br/> |Ouvre des dossiers ou des messages, recherche des dossiers spéciaux et gère les envois de messages.  <br/> |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Obligatoire  <br/> |Recherche et manipule les messages et les sous-dossiers.  <br/> |
|[IMessage](imessageimapiprop.md) <br/> |Obligatoire  <br/> |Manipule les pièces jointes et définit certaines des propriétés d'un message.  <br/> |
|[IMAPITable](imapitableiunknown.md) <br/> |Obligatoire  <br/> |Permet à d'autres objets de présenter des collections de données à divers composants MAPI.  <br/> |
|[IMAPIStatus](imapistatusimapiprop.md) <br/> |Obligatoire  <br/> |Permet aux clients de valider l'état d'une banque de messages et d'effectuer certaines tâches de configuration.  <br/> |
|[IAttach](iattachimapiprop.md) <br/> |Facultatif  <br/> |Accède aux propriétés des pièces jointes des messages si le fournisseur de la banque prend en charge les pièces jointes.  <br/> |
|**IStorage** <br/> |Facultatif  <br/> |Gère les objets de stockage structurés si le fournisseur de banque d'objets prend en charge les pièces jointes OLE.  <br/> |
|**IStream** <br/> |Facultatif  <br/> |Permet à des objets message et Attachment de lire et d'écrire des données dans des objets Stream.  <br/> |
|**IStreamDocfile** <br/> |Facultatif  <br/> |Permet à certains fournisseurs de services d'ouvrir un objet de stockage, tel qu'un fichier composé au format de fichier OLE 2,0.  <br/> |
   
Les informations de base dont vous avez besoin pour implémenter **IMAPIFolder**, **IMessage**, **IMAPIStatus**et **IMAPITable** sont documentées dans les rubriques de référence de ces interfaces. Cette section contient des informations supplémentaires qui sont plus directement liées aux fournisseurs de banques de messages. Les autres interfaces MAPI doivent être implémentées en fonction des informations contenues dans cette section et dans les rubriques de référence appropriées. Pour plus d'informations sur l'implémentation de **IStorage**, **IStream**et **ISTREAMDOCFILE**, voir la section com and ActiveX Object Services dans le kit de développement logiciel (SDK) Windows.
  
## <a name="see-also"></a>Voir aussi



[Développement d’un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)

