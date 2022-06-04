---
title: Récupération des propriétés MAPI
description: Décrit comment les clients et les fournisseurs de services peuvent récupérer les propriétés d’un objet en appelant IMAPIProp::GetProps, IMAPIProp::OpenProperty ou HrGetOneProp.
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: bd3f9f59-9020-46e6-9560-86a7a0eeca20
ms.openlocfilehash: 4c2f69ab97a25c551a9a3854a1db1602ffb867a0
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894886"
---
# <a name="retrieving-mapi-properties"></a>Récupération des propriétés MAPI

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsqu’un client ou un fournisseur de services récupère une propriété d’un objet, l’objet met à disposition la valeur, le type et l’identificateur de la propriété. 
  
Les clients et les fournisseurs de services peuvent récupérer les propriétés d’un objet en appelant l’une des opérations suivantes :
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[HrGetOneProp](hrgetoneprop.md)
  
La méthode **GetProps** est utilisée pour récupérer une ou plusieurs propriétés qui n’ont pas besoin d’une interface spécialisée ou alternative pour l’accès. Cela implique que les propriétés disponibles avec **GetProps** sont petites, telles que des entiers et des valeurs booléennes. 
  
 **Pour récupérer plusieurs propriétés**
  
1. Allouez une structure [SPropTagArray](sproptagarray.md) suffisamment grande pour contenir le nombre de propriétés à récupérer. 
    
2. Définissez le membre **cValues** de la structure **SPropTagArray** sur le nombre de propriétés à récupérer et définissez chaque membre **aulPropTag** sur l’identificateur et le type, si possible, de l’une des propriétés cibles. Si le type est inconnu, définissez-le sur PT_UNSPECIFIED. Si le type et l’identificateur sont inconnus, recherchez ces informations en appelant [IMAPIProp::GetPropList](imapiprop-getproplist.md). **GetPropList** retourne un tableau de balises de propriétés avec toutes les propriétés prises en charge par l’objet. Si seul un nom de propriété est disponible, appelez [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour accéder à l’identificateur associé. 
    
3. Appelez [IMAPIProp::GetProps](imapiprop-getprops.md) pour ouvrir la propriété ou les propriétés. 
    
La méthode **OpenProperty** est utilisée pour ouvrir des propriétés plus volumineuses qui nécessitent une autre interface comme **IStream** ou [IMAPITable](imapitableiunknown.md) pour l’accès. **OpenProperty** est généralement utilisé pour ouvrir des propriétés de chaîne de caractères, binaires et d’objets volumineux et ne peut ouvrir qu’une seule propriété à la fois. Les appelants transmettent l’identificateur de l’interface supplémentaire requise en tant qu’un des paramètres d’entrée. 
  
Parmi les utilisations courantes **d’OpenProperty** , citons l’ouverture **de PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), la propriété qui contient le corps d’un message textuel, **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)), la propriété qui contient un objet ou une pièce jointe de message OLE et **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), la propriété qui contient une table de contenu de conteneur de dossiers ou de carnets d’adresses. 
  
Selon la propriété, une interface différente est demandée à **OpenProperty**. **IStream**, une interface qui permet de lire et d’écrire des données de propriété sous la forme d’un flux d’octets, est généralement utilisé pour accéder à **PR_BODY**. [IMessage](imessageimapiprop.md) ou **IStream** peut être utilisé pour accéder à **PR_ATTACH_DATA_OBJ**. Les pièces jointes de messages incorporés qui sont des messages standard utilisent **IMessage** , tandis que les messages au format TNEF utilisent **IStream**. Étant donné **que PR_CONTAINER_CONTENTS** est un objet de table, il est accessible avec [IMAPITable](imapitableiunknown.md).
  
 **Pour récupérer la propriété PR_ATTACH_DATA_BIN d’une pièce jointe**
  
1. Appelez la fonction [OpenStreamOnFile](openstreamonfile.md) pour ouvrir un flux pour le fichier. 
    
2. Appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du message pour récupérer la propriété **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) avec l’interface **IStream** . Définissez les indicateurs MAPI_MODIFY et MAPI_CREATE. 
    
3. Allouez une structure **STATSTG** et passez-la dans un appel à la méthode **IStream::Stat** du flux de fichiers pour déterminer sa taille. Une autre façon de déterminer la taille du flux consiste à appeler **IStream::Seek** avec l’indicateur STREAM_SEEK_END. 
    
4. Appelez la méthode **IStream::CopyTo** du flux pour copier les données du flux du fichier dans le flux de pièce jointe. 
    
5. Une fois l’opération de copie terminée, relâchez les deux flux en appelant leurs méthodes **IUnknown::Release** . 
    
Quand **IStream** est utilisé pour l’accès aux propriétés, certains fournisseurs de services renvoient automatiquement la taille de la propriété avec le flux. L’appel **d’OpenProperty** avec l’indicateur MAPI_DEFERRED_ERRORS peut retarder l’ouverture de la propriété et le retour de la taille du flux. Si **IStream::Stat** est appelé pour récupérer cette taille après **OpenProperty** avec l’indicateur MAPI_DEFERRED_ERRORS défini, les performances seront affectées, car cette séquence d’appels force un appel de procédure distante supplémentaire. Pour éviter l’atteinte des performances, les clients peuvent appeler n’importe quelle méthode MAPI entre les appels à **OpenProperty** et à **Stat**.
  
La fonction [HrGetOneProp](hrgetoneprop.md) , comme **OpenProperty**, ouvre une propriété à la fois. **HrGetOneProp** ne doit être utilisé que lorsque l’objet cible existe sur l’ordinateur local. Lorsque l’objet cible n’est pas disponible localement, l’utilisation répétée de **HrGetOneProp** peut entraîner plusieurs appels de procédure distante et une dégradation des performances. 
  
Les appelants qui ont besoin de plusieurs propriétés peuvent appeler **HrGetOneProp** ou **OpenProperty** dans une boucle ou effectuer un appel à **GetProps**. L’appel **de GetProps** une fois est plus efficace. 
  
> [!NOTE]
> Les propriétés sécurisées ne sont pas automatiquement disponibles avec d’autres propriétés dans un appel **GetProps**, **HrGetOneProp** ou **GetPropList** . Les propriétés sécurisées doivent être demandées explicitement à l’aide de leurs identificateurs de propriété. 
  
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

