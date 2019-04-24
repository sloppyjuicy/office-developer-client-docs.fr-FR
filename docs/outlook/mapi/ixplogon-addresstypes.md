---
title: IXPLogonAddressTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.AddressTypes
api_type:
- COM
ms.assetid: 5add1f2b-d9e6-4d78-8739-c3848f6e32a3
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: ca68c604152a7a28fb6a5357aa9c012ec7466b5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357210"
---
# <a name="ixplogonaddresstypes"></a>IXPLogon::AddressTypes

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie les types de destinataire gérés par le fournisseur de transport.
  
```cpp
HRESULT AddressTypes(
  ULONG FAR * lpulFlags,
  ULONG FAR * lpcAdrType,
  LPSTR FAR * FAR * lpppszAdrTypeArray,
  ULONG FAR * lpcMAPIUID,
  LPUID FAR * FAR * lpppUIDArray
);
```

## <a name="parameters"></a>Paramètres

 _lpulFlags_
  
> remarquer Masque de des indicateurs qui contrôle le type de chaînes renvoyées. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les chaînes renvoyées sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.
    
 _lpcAdrType_
  
> remarquer Pointeur vers le nombre d'entrées dans le tableau vers lequel pointe le paramètre _lpppszAdrTypeArray_ . 
    
 _lpppszAdrTypeArray_
  
> remarquer Pointeur vers un pointeur vers un tableau de chaînes qui identifient les types de destinataires.
    
 _lpcMAPIUID_
  
> remarquer Pointeur vers le nombre d'entrées dans le tableau vers lequel pointe le paramètre _lpppUIDArray_ . 
    
 _lpppUIDArray_
  
> remarquer Pointeur vers un pointeur vers un tableau de pointeurs vers des structures [MAPIUID](mapiuid.md) qui identifient les types de destinataires. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le fournisseur de transport indiquait les types de destinataires qu'il peut gérer.
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Le spouleur MAPI appelle la méthode **IXPLogon:: AddressTypes** immédiatement après le retour d'un fournisseur de transport d'un appel à la méthode [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) afin que le fournisseur de transport puisse indiquer les types de destinataires qu'il gère. Pour cela, le fournisseur de transport doit renvoyer dans le paramètre _lpppszAdrTypeArray_ un pointeur vers un tableau de pointeurs vers des chaînes, ou renvoyer le pointeur vers un tableau de pointeurs vers **MAPIUID** à partir du paramètre _lpppUIDArray_ les structures, ou transmettre les valeurs des deux paramètres. 
  
Ces deux tableaux sont utilisés pour différents processus d'identification. MAPI et le spouleur MAPI utilisent les structures [MAPIUID](mapiuid.md) dans le tableau _lpppUIDArray_ pour identifier les identificateurs d'entrée de destinataire qui sont directement gérés par le fournisseur de transport ou par le système de messagerie auquel se connecte le fournisseur de transport. . Ni MAPI ni le spouleur MAPI n'étend les adresses à l'aide d'identificateurs d'entrée contenus dans l'une de ces structures **MAPIUID** ; ces structures sont utilisées uniquement pour l'identification du type de destinataire. 
  
Le spouleur MAPI utilise chacune des chaînes du paramètre _lpppszAdrTypeArray_ pour un test de comparaison lorsqu'il détermine quel fournisseur de transport doit gérer les destinataires d'un message sortant. Si la propriété **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) d'un destinataire de message correspond exactement à une chaîne qui identifie l'un des types d'adresse de messagerie fournis par le fournisseur de transport, le fournisseur peut livrer le message à ce destinataire.
  
Si plusieurs fournisseurs de transport peuvent gérer le même type de destinataire, MAPI sélectionne un fournisseur de transport en fonction de l'ordre de priorité de transport indiqué dans le profil de l'application cliente. Pour déterminer le fournisseur de transport à utiliser, le spouleur MAPI analyse toutes les structures **MAPIUID** spécifiées par le fournisseur par ordre de priorité, puis toutes les valeurs de type d'adresse spécifiées par le fournisseur par ordre de priorité. Le premier fournisseur de transport correspondant à un destinataire particulier de cette analyse obtient la première opportunité de gérer ce destinataire. Si ce fournisseur ne gère pas le destinataire, le spouleur MAPI continue l'analyse pour trouver un fournisseur de transport pour un destinataire qui n'est pas encore géré. L'analyse se poursuit jusqu'à ce qu'il n'existe plus de correspondances, auquel cas un rapport de non-remise est généré pour tout destinataire qui n'a pas été géré. 
  
Si le fournisseur prend toujours en charge un ensemble particulier de types de destinataires, le type d'adresse et les tableaux **MAPIUID** que le fournisseur de transport a transmis peuvent être statiques. Si le fournisseur de transport construit ces tableaux de manière dynamique, il peut allouer de la mémoire à l'aide de l'objet de prise en charge précédemment transmis dans l'appel à **TransportLogon**, bien que cela ne soit pas nécessaire.
  
La mémoire utilisée pour le type d'adresse et les tableaux **MAPIUID** doit rester allouée jusqu'au dernier appel à la méthode [IXPLogon:: TransportLogoff](ixplogon-transportlogoff.md) , auquel cas le fournisseur de transport peut libérer de la mémoire, si nécessaire. Le fournisseur de transport ne doit pas modifier le contenu de ces tableaux après qu'il a été renvoyé de l'appel **TransportLogoff** . 
  
Un fournisseur de transport pouvant gérer tout type de destinataire peut renvoyer une valeur NULL dans le paramètre _lpppszAdrTypeArray_ . Les fournisseurs de transport pour les systèmes de messagerie LAN qui utilisent un serveur central pour transmettre les messages sortants à divers systèmes de messagerie étrangers le font généralement. Ce type de fournisseur de transport doit être installé en dernier dans l'ordre de priorité des spouleurs MAPI et MAPI du profil. 
  
Un fournisseur de transport qui ne prend pas en charge les messages sortants qui lui sont envoyés en fonction du type d'adresse doit renvoyer une seule chaîne de longueur nulle dans _lpppszAdrTypeArray_. Si un fournisseur de transport ne prend en charge aucun type de destinataire, il doit transmettre NULL pour la structure **MAPIUID** et une chaîne vide pour le type d'adresse. Les fournisseurs de transport de ce type sont généralement utilisés pour installer un préprocesseur de messages. 
  
## <a name="see-also"></a>Voir aussi



[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[MAPIUID](mapiuid.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

