---
title: Interfaces requises et facultatives pour les fournisseurs de magasins de messages
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: cc62e57e-82a4-4f37-8d1b-7cdf828b951e
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: e907113057f27937c3387401c2b93ee9b2ca6c0a
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62770674"
---
# <a name="required-and-optional-interfaces-for-message-store-providers"></a>Interfaces requises et facultatives pour les fournisseurs de magasins de messages

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI définit un ensemble d’interfaces liées aux fournisseurs de magasins de messages. En raison de la large gamme de fonctionnalités qu’une magasin de messages peut choisir d’implémenter, certaines de ces interfaces sont requises et d’autres non. Le tableau suivant répertorie les interfaces MAPI liées aux fournisseurs de magasins de messages, indique si les interfaces sont obligatoires ou facultatives et décrit leur objectif.
  
|**Interface**|**État**|**Description**|
|:-----|:-----|:-----|
|[IMSProvider](imsprovideriunknown.md) <br/> |Requis  <br/> |Se connecte à une magasin de messages et s’en déconnecte. |
|[IMSLogon](imslogoniunknown.md) <br/> |Requis  <br/> |Ouvre des dossiers ou des messages, vérifie l’identité de la boutique de messages et gère les notifications. |
|[IMsgStore](imsgstoreimapiprop.md) <br/> |Requis  <br/> |Ouvre des dossiers ou des messages, recherche des dossiers spéciaux et gère les envois de messages. |
|[IMAPIFolder](imapifolderimapicontainer.md) <br/> |Requis  <br/> |Recherche et manipule des messages et des sous-foldeurs. |
|[IMessage](imessageimapiprop.md) <br/> |Requis  <br/> |Manipule les pièces jointes et définit certaines propriétés d’un message. |
|[IMAPITable](imapitableiunknown.md) <br/> |Requis  <br/> |Permet à d’autres objets de présenter des collections de données à différents composants MAPI. |
|[IMAPIStatus](imapistatusimapiprop.md) <br/> |Requis  <br/> |Permet aux clients de valider l’état d’un magasin de messages et d’effectuer certaines tâches de configuration. |
|[IAttach](iattachimapiprop.md) <br/> |Facultatif  <br/> |Accède aux propriétés des pièces jointes des messages si le fournisseur de magasins prend en charge les pièces jointes. |
|**IStorage** <br/> |Facultatif  <br/> |Gère les objets de stockage structuré si le fournisseur de magasins prend en charge les pièces jointes d’objets OLE. |
|**IStream** <br/> |Facultatif  <br/> |Permet aux objets message et pièce jointe de lire et d’écrire des données dans des objets de flux. |
|**IStreamDocfile** <br/> |Facultatif  <br/> |Permet à certains fournisseurs de services d’ouvrir un objet de stockage, tel qu’un fichier composé au format de fichier OLE 2.0. |
   
Les informations de base nécessaires pour implémenter **IMAPIFolder**, **IMessage**, **IMAPIStatus** et **IMAPITable** sont documentées dans les rubriques de référence de ces interfaces. Cette section contient des informations supplémentaires plus directement liées aux fournisseurs de magasins de messages. Le reste des interfaces MAPI doit être implémenté en fonction des informations de cette section et des rubriques de référence appropriées. Voir la section COM et ActiveX Object Services dans le SDK Windows pour plus d’informations sur l’implémentation **d’IStorage**, **IStream** et **IStreamDocFile**.
  
## <a name="see-also"></a>Voir aussi



[Développement d’un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)

