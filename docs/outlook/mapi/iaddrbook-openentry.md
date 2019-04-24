---
title: IAddrBookOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.OpenEntry
api_type:
- COM
ms.assetid: bd7746f4-8070-4cc5-8b8e-c527c5847545
description: 'Derni�re modification�: vendredi 1 f�vrier 2013'
ms.openlocfilehash: 293fe5a65c760f61ab0073e0eafc1a606c69050f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287020"
---
# <a name="iaddrbookopenentry"></a>IAddrBook::OpenEntry

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre une entrée de carnet d'adresses et renvoie un pointeur vers une interface qui peut être utilisée pour accéder à l'entrée.
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Paramètres

_cbEntryID_
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ . 
    
_lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée qui représente l'entrée de carnet d'adresses à ouvrir.
    
_lpInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) de l'interface à utiliser pour accéder à l'entrée ouverte. La transmission de la valeur NULL renvoie l'interface standard de l'objet. Pour les utilisateurs de messagerie, l'interface standard est [IMailUser: IMAPIProp](imailuserimapiprop.md). Pour les listes de distribution, il s'agit de [IDistList: IMAPIContainer](idistlistimapicontainer.md) et pour les conteneurs, il s'agit de [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Les appelants peuvent définir _lpInterface_ sur l'interface standard appropriée ou une interface dans la hiérarchie d'héritage. 
    
_ulFlags_
  
> dans Masque de des indicateurs qui contrôle le mode d'ouverture de l'entrée. Les indicateurs suivants peuvent être définis.
    
MAPI_BEST_ACCESS 
  
> Demande que l'entrée soit ouverte avec les autorisations réseau et client maximales autorisées. Par exemple, si le client dispose d'une autorisation en lecture/écriture, le fournisseur de carnet d'adresses doit tenter d'ouvrir l'entrée avec une autorisation en lecture/écriture. Le client peut récupérer le niveau d'accès qui a été accordé en appelant la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de l'entrée ouverte et en récupérant la propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
    
MAPI_CACHE_ONLY
  
> Ouvre une entrée de carnet d'adresses et y accède uniquement à partir du cache. Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d'ouvrir la liste d'adresses globale (LAG) en mode Exchange mis en cache et d'accéder à une entrée de ce carnet d'adresses à partir du cache sans créer de trafic entre le client et le serveur. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.
    
MAPI_DEFERRED_ERRORS 
  
> Permet à l'appel de réussir, éventuellement avant que l'entrée soit entièrement ouverte et disponible, ce qui implique que les appels ultérieurs à l'entrée renvoient une erreur.
    
MAPI_GAL_ONLY
  
> Utilisez uniquement la liste d'adresses globale pour effectuer la résolution de noms. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.
    
  > [!NOTE]
  > Le _ulFlags_ MAPI_GAL_ONLY peut ne pas être défini dans le fichier d'en-tête téléchargeable dont vous disposez actuellement, auquel cas vous pouvez l'ajouter à votre code à l'aide de la valeur suivante: >`#define MAPI_GAL_ONLY (0x00000080)`
  
MAPI_MODIFY 
  
> Demande que l'entrée soit ouverte avec une autorisation en lecture/écriture. Étant donné que les entrées sont ouvertes avec un accès en lecture seule par défaut, les clients ne doivent pas supposer que l'autorisation en lecture/écriture a été accordée, que MAPI_MODIFY soit défini ou non.
    
MAPI_NO_CACHE
  
> N'utilisez pas le carnet d'adresses en mode hors connexion pour effectuer la résolution de noms. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.
    
_lpulObjType_
  
> remarquer Pointeur vers le type de l'entrée ouverte.
    
_lppUnk_
  
> remarquer Pointeur vers un pointeur vers l'entrée ouverte.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'entrée a été ouverte.
    
MAPI_E_NO_ACCESS 
  
> Une tentative d'ouverture d'une entrée pour laquelle l'utilisateur ne dispose pas d'autorisations suffisantes a été effectuée.
    
MAPI_E_NOT_FOUND 
  
> L'entrée représentée par _lpEntryID_ n'existe pas. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L'identificateur d'entrée spécifié dans _lpEntryID_ n'est pas reconnu. Cette valeur est généralement renvoyée si le fournisseur de carnet d'adresses responsable de l'entrée correspondante n'est pas ouvert. 
    
## <a name="remarks"></a>Remarques

Les clients et les fournisseurs de services appellent la méthode **IAddrBook:: OpenEntry** pour ouvrir une entrée de carnet d'adresses. MAPI transfère l'appel au fournisseur de carnet d'adresses approprié, en fonction de la structure [MAPIUID](mapiuid.md) incluse dans l'identificateur d'entrée passé dans le paramètre _lpEntryID_ . Le fournisseur de carnet d'adresses ouvre l'entrée en lecture seule sauf si l'indicateur MAPI_MODIFY ou MAPI_BEST_ACCESS dans le paramètre _ulFlags_ est défini. Toutefois, ces indicateurs sont des suggestions. Si le fournisseur de carnet d'adresses n'autorise pas la modification de l'entrée demandée, il renvoie MAPI_E_NO_ACCESS. 
  
Le paramètre _lpInterface_ indique l'interface qui doit être utilisée pour accéder à l'entrée ouverte. Le passage de la valeur NULL dans _lpInterface_ indique que l'interface MAPI standard pour ce type d'entrée doit être utilisée. Étant donné que le fournisseur de carnet d'adresses peut renvoyer une interface différente de celle suggérée par le paramètre _lpInterface_ , l'appelant doit vérifier la valeur renvoyée dans le paramètre _lpulObjType_ pour déterminer si le type d'objet retourné est ce qui était attendu. Si le type d'objet n'est pas du type attendu, l'appelant peut effectuer un cast du paramètre _lppUnk_ en un type plus approprié. 
  
## <a name="see-also"></a>Voir aussi

- [IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

