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
ms.openlocfilehash: 9666c551543cefd12ee8c902db1a2372aab20632
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328643"
---
# <a name="retrieving-mapi-properties"></a>Récupération des propriétés MAPI

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu'un client ou un fournisseur de services récupère une propriété à partir d'un objet, l'objet rend disponible la valeur, le type et l'identificateur de la propriété. 
  
Les clients et les fournisseurs de services peuvent récupérer les propriétés d'un objet en appelant l'une des méthodes suivantes:
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[HrGetOneProp](hrgetoneprop.md)
  
La méthode **GetProps** est utilisée pour récupérer une ou plusieurs propriétés qui n'ont pas besoin d'une interface spécialisée ou alternative pour l'accès. Cela signifie que les propriétés disponibles avec **GetProps** sont petites, telles que des nombres entiers et des valeurs booléennes. 
  
 **Pour récupérer plusieurs propriétés**
  
1. AlLouez une structure [SPropTagArray](sproptagarray.md) suffisamment grande pour contenir le nombre de propriétés à récupérer. 
    
2. Définissez le membre **cValues** de la structure **SPropTagArray** sur le nombre de propriétés à récupérer et définissez chaque membre **aulPropTag** sur l'identificateur et tapez, dans la mesure du possible, l'une des propriétés cibles. Si le type est Unknown, définissez-le sur PT_UNSPECIFIED. Si le type et l'identificateur sont inconnus, recherchez ces informations en appelant [IMAPIProp:: GetPropList](imapiprop-getproplist.md). **GetPropList** renvoie un tableau de balises de propriété avec toutes les propriétés prises en charge par l'objet. Si seul un nom de propriété est disponible, appelez [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) pour accéder à l'identificateur associé. 
    
3. Appelez [IMAPIProp:: GetProps](imapiprop-getprops.md) pour ouvrir la ou les propriétés. 
    
La méthode **OpenProperty** est utilisée pour ouvrir des propriétés plus volumineuses qui nécessitent une interface alternative telle que **IStream** ou [IMAPITable](imapitableiunknown.md) pour Access. **OpenProperty** est généralement utilisé pour ouvrir des propriétés de chaîne de caractères volumineuses, binaires et d'objets, et ne peut ouvrir qu'une seule propriété à la fois. Les appelants passent dans l'identificateur de l'interface supplémentaire requise comme l'un des paramètres d'entrée. 
  
Certaines des utilisations courantes de **OpenProperty** incluent l'ouverture de **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), la propriété qui contient le corps d'un message texte, **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)), la propriété qui contient un Objet OLE ou pièce jointe de message et **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), la propriété qui contient une table de contenu de conteneur de carnet d'adresses ou de dossier. 
  
En fonction de la propriété, une interface différente est demandée à partir de **OpenProperty**. **IStream**, une interface qui permet la lecture et l'écriture des données de propriété sous la forme d'un flux d'octets, est généralement utilisée pour accéder à **PR_BODY**. [IMessage](imessageimapiprop.md) ou **IStream** peuvent être utilisés pour accéder à **PR_ATTACH_DATA_OBJ**. Les pièces jointes des messages incorporés qui sont des messages standard utilisent **IMessage** tandis que les messages au format TNEF utilisent **IStream**. Étant donné que **PR_CONTAINER_CONTENTS** est un objet table, il est accessible avec une opération [IMAPITable](imapitableiunknown.md).
  
 **Pour récupérer la propriété PR_ATTACH_DATA_BIN d'une pièce jointe**
  
1. Appelez la fonction [OpenStreamOnFile](openstreamonfile.md) pour ouvrir un flux pour le fichier. 
    
2. Appelez la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) du message pour extraire la **propriété PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) à l'aide de l'interface **IStream** . Définissez les deux indicateurs MAPI_MODIFY et MAPI_CREATE. 
    
3. AlLouez une structure **STATSTG** et transmettez-la dans un appel à la méthode **IStream:: stat** du flux de fichier afin de déterminer sa taille. Une autre façon de déterminer la taille du flux est d'appeler **IStream:: Seek** avec l'indicateur STREAM_SEEK_END. 
    
4. Appelez la méthode **IStream:: CopyTo** du flux pour copier les données du flux du fichier dans le flux de pièces jointes. 
    
5. Une fois l'opération de copie terminée, libérez les deux flux en appelant leurs méthodes **IUnknown:: Release** . 
    
Lorsque **IStream** est utilisé pour l'accès à la propriété, certains fournisseurs de services envoient automatiquement la taille de la propriété avec le flux. L'appel de **OpenProperty** avec l'indicateur MAPI_DEFERRED_ERRORS peut retarder l'ouverture de la propriété et le retour de la taille du flux. Si **IStream:: stat** est appelé pour récupérer cette taille une fois que **OpenProperty** avec l'indicateur MAPI_DEFERRED_ERRORS défini, les performances seront affectées, car cette séquence d'appels force un appel de procédure distante supplémentaire. Pour éviter l'impact sur les performances, les clients peuvent appeler n'importe quelle méthode MAPI entre les appels vers **OpenProperty** et **Stat**.
  
La fonction [HrGetOneProp](hrgetoneprop.md) , comme **OpenProperty**, ouvre une propriété à la fois. **HrGetOneProp** doit être utilisé uniquement lorsque l'objet cible existe sur l'ordinateur local. Lorsque l'objet cible n'est pas disponible localement, l'utilisation répétée de **HrGetOneProp** peut entraîner plusieurs appels de procédure distante et une dégradation des performances. 
  
Les appelants qui ont besoin de plusieurs propriétés peuvent appeler **HrGetOneProp** ou **OpenProperty** dans une boucle ou effectuer un appel à **GetProps**. L'appel de **GetProps** est plus efficace. 
  
> [!NOTE]
> Les propriétés sécurisées ne sont pas automatiquement disponibles pour les autres propriétés dans un appel **GetProps**, **HrGetOneProp**ou **GetPropList** . Les propriétés sécurisées doivent être explicitement demandées à l'aide de leurs identificateurs de propriété. 
  
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

