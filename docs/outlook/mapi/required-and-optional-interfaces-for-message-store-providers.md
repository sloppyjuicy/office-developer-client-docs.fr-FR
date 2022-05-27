---
title: Interfaces obligatoires et facultatives pour les fournisseurs de magasin de messages
description: Décrit les interfaces obligatoires et facultatives pour les fournisseurs de magasins de messages. MAPI définit un ensemble d’interfaces liées aux fournisseurs de magasins de messages.
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: cc62e57e-82a4-4f37-8d1b-7cdf828b951e
ms.openlocfilehash: 641185873e0f8c5fc5db6d7ef946137bc0c29bbb
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65751615"
---
# <a name="required-and-optional-interfaces-for-message-store-providers"></a>Interfaces obligatoires et facultatives pour les fournisseurs de magasin de messages

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI définit un ensemble d’interfaces liées aux fournisseurs de magasins de messages. En raison de la large gamme de fonctionnalités qu’un magasin de messages peut choisir d’implémenter, certaines de ces interfaces sont requises et d’autres non. Le tableau suivant répertorie les interfaces MAPI liées aux fournisseurs de magasins de messages, spécifie si les interfaces sont obligatoires ou facultatives et décrit leur objectif.
  
|**Interface**|**État**|**Description**|
|:-----|:-----|:-----|
|[IMSProvider](imsprovideriunknown.md) <br/> |Requis  <br/> |Ouvre une session vers et hors d’un magasin de messages. |
|[IMSLogon](imslogoniunknown.md) <br/> |Requis  <br/> |Ouvre des dossiers ou des messages, vérifie l’identité du magasin de messages et gère les notifications. |
|[IMsgStore](imsgstoreimapiprop.md) <br/> |Requis  <br/> |Ouvre des dossiers ou des messages, recherche des dossiers spéciaux et gère les soumissions de messages. |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Requis  <br/> |Recherche et manipule les messages et les sous-dossiers. |
|[Imessage](imessageimapiprop.md) <br/> |Requis  <br/> |Manipule les pièces jointes et définit certaines propriétés d’un message. |
|[IMAPITable](imapitableiunknown.md) <br/> |Requis  <br/> |Permet à d’autres objets de présenter des collections de données à différents composants MAPI. |
|[IMAPIStatus](imapistatusimapiprop.md) <br/> |Requis  <br/> |Permet aux clients de valider l’état d’un magasin de messages et d’effectuer certaines tâches de configuration. |
|[IAttach](iattachimapiprop.md) <br/> |Facultatif  <br/> |Accède aux propriétés des pièces jointes de message si le fournisseur du magasin prend en charge les pièces jointes de fichier. |
|**IStorage** <br/> |Facultatif  <br/> |Gère les objets de stockage structurés si le fournisseur de magasin prend en charge les pièces jointes d’objet OLE. |
|**IStream** <br/> |Facultatif  <br/> |Permet aux objets de message et de pièce jointe de lire et d’écrire des données dans des objets de flux. |
|**IStreamDocfile** <br/> |Facultatif  <br/> |Permet à certains fournisseurs de services d’ouvrir un objet de stockage, tel qu’un fichier composé au format de fichier OLE 2.0. |
   
Les informations de base dont vous avez besoin pour **implémenter IMAPIFolder**, **IMessage**, **IMAPIStatus** et **IMAPITable** sont documentées dans les rubriques de référence de ces interfaces. Cette section contient des informations supplémentaires qui sont plus directement liées aux fournisseurs de magasins de messages. Le reste des interfaces MAPI doit être implémenté en fonction des informations contenues dans cette section et dans les rubriques de référence appropriées. Pour plus d’informations sur l’implémentation **d’IStorage**, **IStream** et **IStreamDocFile**, consultez la section COM et ActiveX Object Services du SDK Windows.
  
## <a name="see-also"></a>Voir aussi



[Développement d’un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)

