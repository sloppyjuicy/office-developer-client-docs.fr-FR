---
title: IXPLogonAddressTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.AddressTypes
api_type:
- COM
ms.assetid: 5add1f2b-d9e6-4d78-8739-c3848f6e32a3
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3423391ce6744f7a21bed337778fd8a76aa15d4c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587810"
---
# <a name="ixplogonaddresstypes"></a>IXPLogon::AddressTypes

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie les types de destinataires gérés par le fournisseur de transport.
  
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
  
> [out] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les chaînes renvoyées sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 _lpcAdrType_
  
> [out] Pointeur vers le nombre d’entrées du tableau pointées par le _paramètre lpppszAdrTypeArray._ 
    
 _lpppszAdrTypeArray_
  
> [out] Pointeur vers un pointeur vers un tableau de chaînes qui identifient les types de destinataires.
    
 _lpcMAPIUID_
  
> [out] Pointeur vers le nombre d’entrées du tableau pointées par le _paramètre lpppUIDArray._ 
    
 _lpppUIDArray_
  
> [out] Pointeur vers un pointeur vers un tableau de pointeurs vers des structures [MAPIUID](mapiuid.md) qui identifient les types de destinataires. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le fournisseur de transport a indiqué avec succès les types de destinataires qu’il peut gérer.
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Lepooler MAPI appelle la méthode **IXPLogon::AddressTypes** immédiatement après le retour d’un fournisseur de transport à partir d’un appel à la méthode [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) afin que le fournisseur de transport puisse indiquer les types de destinataires qu’il gère. Pour indiquer cela, le fournisseur de transport doit transmettre dans le paramètre  _lpppszAdrTypeArray_ un pointeur vers un tableau de pointeurs vers des chaînes, ou revenir dans le paramètre  _lpppUIDArray_ un pointeur vers un tableau de pointeurs vers des structures **MAPIUID,** ou transmettre des valeurs dans les deux paramètres. 
  
Ces deux tableaux sont utilisés pour différents processus d’identification. MAPI et le spouleur MAPI utilisent les structures [MAPIUID](mapiuid.md) dans le tableau  _lpppUIDArray_ pour identifier les identificateurs d’entrée de destinataire qui sont directement gérés par le fournisseur de transport ou par le système de messagerie auquel le fournisseur de transport se connecte. Ni MAPI, ni le spouleur MAPI ne développe les adresses à l’aide des identificateurs d’entrée contenus dans l’une de ces structures **MAPIUID** ; Ces structures sont utilisées uniquement pour l’identification du type de destinataire. 
  
Lepooler MAPI utilise chacune des chaînes du paramètre  _lpppszAdrTypeArray_ pour un test de comparaison lorsqu’il détermine le fournisseur de transport qui doit gérer les destinataires d’un message sortant. Si la propriété **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) d’un destinataire de message correspond exactement à une chaîne qui identifie l’un des types d’adresse de messagerie que le fournisseur de transport fournit, le fournisseur peut remettre le message à ce destinataire.
  
Si plusieurs fournisseurs de transport peuvent gérer le même type de destinataire, MAPI sélectionne un fournisseur de transport en fonction de l’ordre de priorité de transport indiqué dans le profil de l’application cliente. Pour déterminer le fournisseur de transport à utiliser, le spouleur MAPI analyse toutes les structures **MAPIUID** spécifiées par le fournisseur dans l’ordre de priorité, puis toutes les valeurs de type d’adresse spécifiées par le fournisseur dans l’ordre de priorité. Le premier fournisseur de transport à faire correspondre un destinataire particulier dans cette analyse obtient la première opportunité de gérer ce destinataire. Si ce fournisseur ne gère pas le destinataire, lepooler MAPI poursuit l’analyse pour rechercher un fournisseur de transport pour un destinataire qui n’a pas encore été géré. L’analyse se poursuit jusqu’à ce qu’aucune autre correspondance ne soit trouvée, auquel moment un rapport de non-découverte est généré pour tout destinataire qui n’a pas été géré. 
  
Si le fournisseur prend toujours en charge un ensemble particulier de types de destinataires, le type d’adresse et les tableaux **MAPIUID** transmis par le fournisseur de transport peuvent être statiques. Si le fournisseur de transport construit dynamiquement ces tableaux, il peut allouer de la mémoire à l’aide de l’objet de support qui a été passé précédemment dans l’appel à **TransportLogon,** bien que cela ne soit pas nécessaire.
  
La mémoire utilisée pour le type d’adresse et les tableaux **MAPIUID** doit rester allouée jusqu’à l’appel final à la méthode [IXPLogon::TransportLogoff,](ixplogon-transportlogoff.md) à laquelle le fournisseur de transport peut libérer de la mémoire, si nécessaire. Le fournisseur de transport ne doit pas modifier le contenu de ces tableaux après son retour de **l’appel TransportLogoff.** 
  
Un fournisseur de transport qui peut gérer n’importe quel type de destinataire peut renvoyer la valeur NULL dans le paramètre _lpppszAdrTypeArray._ Les fournisseurs de transport pour les systèmes de messagerie laN qui utilisent un serveur central pour remettre des messages sortants à différents systèmes de messages étrangers le font généralement. Ce type de fournisseur de transport doit être installé en dernier dans l’ordre de priorité dupooler MAPI et MAPI des fournisseurs de transport dans le profil. 
  
Un fournisseur de transport qui ne prend pas en charge les messages sortants qui lui sont envoyés en fonction du type d’adresse doit renvoyer une seule chaîne de longueur nulle dans  _lpppszAdrTypeArray_. Si un fournisseur de transport ne prend en charge aucun type de destinataire, il doit transmettre null pour la structure **MAPIUID** et une chaîne vide pour le type d’adresse. Les fournisseurs de transport de ce type sont le plus couramment utilisés pour installer un préprocesseur de message. 
  
## <a name="see-also"></a>Voir aussi



[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[MAPIUID](mapiuid.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

