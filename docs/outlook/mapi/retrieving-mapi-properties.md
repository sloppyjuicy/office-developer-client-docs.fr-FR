---
title: Récupération des propriétés MAPI
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: bd3f9f59-9020-46e6-9560-86a7a0eeca20
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: 8c52f8a6768f43190bff86c8fe71c884102a4c91
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624313"
---
# <a name="retrieving-mapi-properties"></a>Récupération des propriétés MAPI

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu’un client ou un fournisseur de services récupère une propriété à partir d’un objet, l’objet met à disposition la valeur, le type et l’identificateur de la propriété. 
  
Les clients et les fournisseurs de services peuvent récupérer les propriétés d’un objet en appelant l’une des solutions suivantes :
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[HrGetOneProp](hrgetoneprop.md)
  
La **méthode GetProps** permet de récupérer une ou plusieurs propriétés qui n’ont pas besoin d’une interface spécialisée ou alternative pour l’accès. Cela implique que les propriétés disponibles avec **GetProps** sont de petite taille, telles que les nombres integers et les valeurs booléiennes. 
  
 **Pour récupérer plusieurs propriétés**
  
1. Allouez une structure [SPropTagArray](sproptagarray.md) suffisamment grande pour contenir le nombre de propriétés à récupérer. 
    
2. Définissez le membre **cValues** de la structure **SPropTagArray** sur le nombre de propriétés à récupérer et définissez chaque membre **aulPropTag** sur l’identificateur et le type, si possible, de l’une des propriétés cibles. Si le type est inconnu, définissez-le sur PT_UNSPECIFIED. Si le type et l’identificateur sont inconnus, recherchez ces informations en appelant [IMAPIProp::GetPropList](imapiprop-getproplist.md). **GetPropList renvoie** un tableau de balises de propriétés avec toutes les propriétés de l’objet pris en charge. Si seul un nom de propriété est disponible, appelez [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour accéder à l’identificateur associé. 
    
3. Appelez [IMAPIProp::GetProps](imapiprop-getprops.md) pour ouvrir la ou les propriétés. 
    
La **méthode OpenProperty** permet d’ouvrir des propriétés plus volumineuses qui nécessitent une autre interface telle que **IStream** ou [IMAPITable](imapitableiunknown.md) pour l’accès. **OpenProperty est** généralement utilisé pour ouvrir des propriétés de chaîne de caractères, binaires et objets de grande taille et ne peut ouvrir qu’une seule propriété à la fois. Les appelants passent l’identificateur de l’interface supplémentaire requise comme l’un des paramètres d’entrée. 
  
Certaines des utilisations courantes **d’OpenProperty** incluent l’ouverture de **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), la propriété qui contient le corps d’un message texte, **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)), la propriété qui contient un objet OLE ou une pièce jointe de message, et **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), la propriété qui contient une table de contenu de conteneur de dossier ou de carnet d’adresses. 
  
En fonction de la propriété, une interface différente est demandée à partir **d’OpenProperty**. **IStream**, une interface qui permet aux données de propriété d’être lues et écrites en tant que flux d’octets, est généralement utilisé pour accéder **à PR_BODY**. [IMessage ou](imessageimapiprop.md) **IStream** peut être utilisé pour accéder à **PR_ATTACH_DATA_OBJ**. Les pièces jointes de messages incorporés qui sont des messages standard utilisent **IMessage,** tandis que les messages au format TNEF **utilisent IStream**. Comme **PR_CONTAINER_CONTENTS** est un objet table, il est accessible avec [IMAPITable](imapitableiunknown.md).
  
 **Pour récupérer la propriété d’PR_ATTACH_DATA_BIN pièce jointe**
  
1. Appelez la [fonction OpenStreamOnFile pour](openstreamonfile.md) ouvrir un flux pour le fichier. 
    
2. Appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du message pour récupérer la propriété **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) avec l’interface **IStream.** Définissez les indicateurs MAPI_MODIFY et MAPI_CREATE de l’indicateur. 
    
3. Allouez une structure **STATSTG** et passez-la dans un appel à la méthode **IStream::Stat** du flux de fichiers pour déterminer sa taille. Une autre façon de déterminer la taille du flux consiste à appeler **IStream::Seek** avec l’indicateur STREAM_SEEK_END. 
    
4. Appelez la méthode **IStream::CopyTo** du flux pour copier les données du flux du fichier dans le flux de pièce jointe. 
    
5. Lorsque l’opération de copie est terminée, relâchez les deux flux en appelant leurs méthodes **IUnknown::Release.** 
    
Lorsque **IStream est** utilisé pour l’accès aux propriétés, certains fournisseurs de services renvoient automatiquement la taille de la propriété avec le flux. **L’appel d’OpenProperty** avec MAPI_DEFERRED_ERRORS’indicateur peut retarder l’ouverture de la propriété et le retour de la taille du flux. Si **IStream::Stat** est appelé pour récupérer cette taille après **OpenProperty** avec l’indicateur MAPI_DEFERRED_ERRORS définie, les performances seront impactées car cette séquence d’appels force un appel de procédure distante supplémentaire. Pour éviter les performances, les clients peuvent appeler n’importe quelle méthode MAPI entre les appels à **OpenProperty** et **à Stat**.
  
La [fonction HrGetOneProp,](hrgetoneprop.md) comme **OpenProperty,** ouvre une propriété à la fois. **HrGetOneProp ne** doit être utilisé que lorsque l’objet cible existe sur l’ordinateur local. Lorsque l’objet cible n’est pas disponible localement, l’utilisation répétée de **HrGetOneProp** peut entraîner plusieurs appels de procédure distante et une dégradation des performances. 
  
Les appelants qui ont besoin de plusieurs propriétés peuvent appeler **HrGetOneProp** ou **OpenProperty** dans une boucle ou effectuer un appel **à GetProps.** Appeler **GetProps une** fois est plus efficace. 
  
> [!NOTE]
> Les propriétés sécurisées ne sont pas automatiquement disponibles avec d’autres propriétés dans un appel **GetProps,** **HrGetOneProp** ou **GetPropList.** Les propriétés sécurisées doivent être demandées explicitement à l’aide de leurs identificateurs de propriété. 
  
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

