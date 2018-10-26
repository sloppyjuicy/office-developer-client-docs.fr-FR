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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 65d633f0c2b0ce56793eaa55a417b5d6a816d449
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589846"
---
# <a name="ixplogonaddresstypes"></a>IXPLogon::AddressTypes

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie les types de destinataires qui gère le fournisseur de transport.
  
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
  
> [out] Masque de bits d’indicateurs qui contrôle le type de chaînes renvoyées. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les chaînes retournées sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 _lpcAdrType_
  
> [out] Un pointeur vers le nombre d’entrées dans le tableau indiqué par le paramètre _lpppszAdrTypeArray_ . 
    
 _lpppszAdrTypeArray_
  
> [out] Pointeur vers un pointeur vers un tableau de chaînes qui identifient les types de destinataires.
    
 _lpcMAPIUID_
  
> [out] Un pointeur vers le nombre d’entrées dans le tableau indiqué par le paramètre _lpppUIDArray_ . 
    
 _lpppUIDArray_
  
> [out] Pointeur vers un pointeur vers un tableau de pointeurs vers des structures [MAPIUID](mapiuid.md) qui identifient les types de destinataires. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le fournisseur de transport indiqué correctement les types de destinataires qu’il peut traiter.
    
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Le spouleur MAPI appelle la méthode **IXPLogon::AddressTypes** immédiatement après qu’un fournisseur de transport renvoie à partir d’un appel à la méthode [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) afin que le fournisseur de transport peut indiquer quels types de destinataires qu’il gère. Pour indiquer cela, le fournisseur de transport doit passer dans le paramètre _lpppszAdrTypeArray_ un pointeur vers un tableau de pointeurs vers des chaînes, ou passer dans le paramètre _lpppUIDArray_ un pointeur vers un tableau de pointeurs vers **MAPIUID** structures, ou passer de valeurs dans les deux paramètres. 
  
Ces deux tableaux est utilisés pour les processus d’identification différent. MAPI et le spouleur MAPI utilisent les structures [MAPIUID](mapiuid.md) dans le tableau _lpppUIDArray_ pour identifier les identificateurs d’entrée du destinataire qui sont directement gérés par le fournisseur de transport ou par le système de messagerie à laquelle se connecte le fournisseur de transport . Le spouleur MAPI ni MAPI développe des adresses à l’aide d’identificateurs d’entrée contenues dans une de ces structures **MAPIUID** ; Ces structures sont utilisés uniquement pour l’identification du type de destinataire. 
  
Le spouleur MAPI utilise chacune des chaînes dans le paramètre _lpppszAdrTypeArray_ pour un test de comparaison lorsqu’il détermine quel fournisseur de transport doit gérer les destinataires d’un message sortant. Si la propriété de **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) d’un destinataire de message correspond exactement à une chaîne qui identifie un des types d’adresse messagerie qui fournit le fournisseur de transport, le fournisseur peut remettre le message au destinataire.
  
Si plusieurs fournisseurs de transport peuvent gérer le même type de destinataire, MAPI sélectionne un fournisseur de transport selon l’ordre de priorité transport indiqué dans le profil de l’application cliente. Pour déterminer le fournisseur de transport à utiliser, le spouleur MAPI analyse tous les structures **MAPIUID** fournisseur spécifié dans l’ordre de priorité et ensuite tous les adresse spécifiée par fournisseur de valeurs de type dans l’ordre de priorité. Le premier fournisseur de transport pour correspondre à un destinataire particulier dans cette analyse Obtient la première possibilité de gérer ce destinataire. Si ce fournisseur ne gère pas le destinataire, le spouleur MAPI continue l’analyse pour trouver un fournisseur de transport pour n’importe quel destinataire n’est pas encore géré. L’analyse se poursuit jusqu'à ce qu’aucune correspondance n’est détectée, à partir de laquelle un rapport de non-remise est généré pour n’importe quel destinataire n’est pas géré. 
  
Si le fournisseur prend toujours en charge un ensemble particulier de types de destinataires, le type d’adresse et tableaux **MAPIUID** que le fournisseur de transport passé peuvent être statiques. Si le fournisseur de transport construit dynamiquement ces tableaux, elle peut allouer de la mémoire à l’aide de l’objet de prise en charge qui a été précédemment passée dans l’appel à **TransportLogon**, bien que cela n’est pas nécessaire.
  
La mémoire utilisée pour le type d’adresse et tableaux **MAPIUID** doit rester allouée jusqu'à ce que le dernier appel à la méthode [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) , date à laquelle le fournisseur de transport peut libérer de la mémoire, si nécessaire. Le fournisseur de transport ne doit pas modifier le contenu de ces tableaux après le retour de l’appel **TransportLogoff** . 
  
Un fournisseur de transport qui peut gérer n’importe quel type de destinataire peut renvoyer la valeur NULL dans le paramètre _lpppszAdrTypeArray_ . Fournisseurs de transport pour les systèmes messages basée sur le réseau local qui permet de remettre les messages sortants à différents systèmes de messagerie étrangers généralement un serveur central pour cela. Ce type de fournisseur de transport doit être installé en dernier dans le MAPI et MAPI ordre de priorité spouleur des fournisseurs de transport dans le profil. 
  
Un fournisseur de transport qui ne prend pas en charge des messages sortants sont réparties selon le type d’adresse doit renvoyer une seule chaîne de longueur nulle dans _lpppszAdrTypeArray_. Si un fournisseur de transport prend en charge aucun type de destinataire, il doit passer la valeur NULL pour la structure **MAPIUID** et une chaîne vide pour le type d’adresse. Fournisseurs de transport de ce type sont plus fréquemment utilisés pour installer un préprocesseur de message. 
  
## <a name="see-also"></a>Voir aussi



[IXPLogon::TransportLogoff](ixplogon-transportlogoff.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[MAPIUID](mapiuid.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

