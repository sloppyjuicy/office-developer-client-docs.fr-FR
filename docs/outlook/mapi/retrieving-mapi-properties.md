---
title: Récupération des propriétés MAPI
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bd3f9f59-9020-46e6-9560-86a7a0eeca20
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: 1404239a54f9b8991099a66831e3364d9a683d1d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566333"
---
# <a name="retrieving-mapi-properties"></a>Récupération des propriétés MAPI

 
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Lorsqu’un client ou fournisseur de services récupère une propriété d’un objet, l’objet rend disponibles identificateur, type et la valeur de propriété. 
  
Clients et fournisseurs de services peuvent récupérer les propriétés d’un objet en appelant une des options suivantes :
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[HrGetOneProp](hrgetoneprop.md)
  
La méthode **GetProps** est utilisée pour récupérer une ou plusieurs propriétés qui ne doivent pas une interface spécialisée ou de l’autre pour l’accès. Cela implique que les propriétés disponibles avec **GetProps** sont petites, tels que des entiers et les valeurs booléennes. 
  
 **Pour extraire plusieurs propriétés**
  
1. Allouez une structure [SPropTagArray](sproptagarray.md) suffisante pour contenir le nombre de propriétés à récupérer. 
    
2. Définissez le membre **cValues** de la structure **SPropTagArray** et le nombre de propriétés de récupérer et de définir la mesure du possible, les chaque membre **aulPropTag** l’identificateur et le type d’une des propriétés de la cible. Si le type est inconnu, affectez-lui PT_UNSPECIFIED. Si le type et l’identificateur sont inconnues, recherchez ces informations en appelant [IMAPIProp::GetPropList](imapiprop-getproplist.md). **GetPropList** renvoie un tableau de balise de propriété avec toutes les propriétés de l’objet pris en charge. Si seul un nom de propriété est disponible, appelez [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour accéder à l’identificateur associé. 
    
3. Appelez [IMAPIProp::GetProps](imapiprop-getprops.md) pour ouvrir les propriétés. 
    
La méthode **OpenProperty** est utilisée pour ouvrir les propriétés de plus grandes qui nécessitent une interface de substitution tel que **IStream** ou [IMAPITable](imapitableiunknown.md) pour access. **OpenProperty** est généralement utilisé pour ouvrir la chaîne de caractères de grande taille et propriétés de l’objet binaire et peut uniquement ouvrir une propriété à la fois. Les appelants passez l’identificateur de l’interface supplémentaire qui est requis en tant qu’un des paramètres d’entrée. 
  
Les utilisations courantes de **OpenProperty** parmi l’ouverture **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), la propriété contenant le corps d’un message textuel, **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)), la propriété qui contient un Objet OLE ou message jointe et **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), la propriété qui contient un tableau contenu de dossier ou l’adresse livre conteneur. 
  
En fonction de la propriété, une autre interface **OpenProperty**est demandée. **IStream**, une interface qui permet de lire et écrire en tant que flux d’octets, des données de propriété est généralement utilisé pour accéder aux **PR_BODY**. [IMessage](imessageimapiprop.md) ou **IStream** peut être utilisé pour accéder aux **PR_ATTACH_DATA_OBJ**. Pièces jointes de messages incorporés qui sont des messages standards utilisent **IMessage** tandis que les messages au format TNEF utiliser **IStream**. Étant donné que **PR_CONTAINER_CONTENTS** est un objet table, il est accessible avec [IMAPITable](imapitableiunknown.md).
  
 **Pour récupérer PR_ATTACH_DATA_BIN propriété d’une pièce jointe**
  
1. Appelez la fonction [OpenStreamOnFile](openstreamonfile.md) pour ouvrir un flux de données pour le fichier. 
    
2. Appeler la méthode de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du message pour récupérer la propriété **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) avec l’interface **IStream** . Définir des indicateurs n’et de MAPI_CREATE. 
    
3. Allouer une structure **STATSTG** et transmettez-le à un appel à la méthode de **IStream::Stat** du flux de fichier afin de déterminer sa taille. Une autre manière de déterminer la taille du flux est d’appeler **IStream::Seek** avec l’indicateur STREAM_SEEK_END. 
    
4. Appelez la méthode du flux **IStream::CopyTo** pour copier les données de flux de données du fichier dans le flux de pièce jointe. 
    
5. Lorsque l’opération de copie est terminée, les deux flux de publication en appelant leurs méthodes **IUnknown::Release** . 
    
Lorsque **IStream** est utilisée pour l’accès à la propriété, certains fournisseurs de services envoient automatiquement la taille de la propriété avec l’objet stream. Indicateur appelant **OpenProperty** avec la MAPI_DEFERRED_ERRORS peut retarder l’ouverture de la propriété et le retour de la taille du flux. Si **IStream::Stat** est appelée pour récupérer cette taille après **OpenProperty** avec la MAPI_DEFERRED_ERRORS l’indicateur est défini, performances seront affectées, car cette séquence d’appels force un appel de procédure distante supplémentaire. Pour éviter l’impact sur les performances, les clients peuvent appeler n’importe quelle méthode MAPI entre les appels **OpenProperty** et **jours fériés**.
  
La fonction [HrGetOneProp](hrgetoneprop.md) , comme **OpenProperty**, ouvre une propriété à la fois. **HrGetOneProp** doit être utilisé uniquement lorsque l’objet cible existe sur l’ordinateur local. Lorsque l’objet cible n’est pas disponible localement, à l’aide de **HrGetOneProp** à plusieurs reprises peut entraîner une dégradation des performances et de plusieurs appels de procédure distante. 
  
Les appelants nécessitant plusieurs propriétés peuvent appeler **HrGetOneProp** ou **OpenProperty** dans une boucle ou émettre un appel à **GetProps**. Une fois l’appel **GetProps** est plus efficace. 
  
> [!NOTE]
> Propriétés sécurisées ne sont pas automatiquement disponibles à d’autres propriétés dans un appel **GetProps**, **HrGetOneProp**ou **GetPropList** . Propriétés sécurisées doivent être demandées explicitement à l’aide de leurs identificateurs de propriété. 
  
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

