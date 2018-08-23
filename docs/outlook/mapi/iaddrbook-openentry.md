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
ms.openlocfilehash: 4d380f784094064232cdb7369080612ba9ccac0e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576868"
---
# <a name="iaddrbookopenentry"></a>IAddrBook::OpenEntry

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Ouvre une entrée de carnet d’adresses et retourne un pointeur vers une interface qui peut servir à accéder à l’entrée.
  
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
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
_lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée qui représente l’entrée du carnet d’adresses à ouvrir.
    
_lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) de l’interface à utiliser pour accéder à l’entrée open. Passage de NULL renvoie interface standard de l’objet. Pour les utilisateurs de messagerie, l’interface standard est [IMailUser : IMAPIProp](imailuserimapiprop.md). Pour les listes de distribution, il est [IDistList : IMAPIContainer](idistlistimapicontainer.md) et pour les conteneurs, il est [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Les appelants peuvent définir _lpInterface_ à l’interface standard ou d’une interface dans la hiérarchie d’héritage. 
    
_ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’entrée est ouvert. Les indicateurs suivants peuvent être définis.
    
MAPI_BEST_ACCESS 
  
> Demandes que l’entrée s’ouvre avec les autorisations maximales autorisées réseau et le client. Par exemple, si le client a l’autorisation de lecture/écriture, le fournisseur de carnet d’adresses doit essayer ouvrir l’entrée avec une autorisation en lecture-écriture. Le client peut extraire le niveau d’accès qui a été accordé par l’appel de méthode de [IMAPIProp::GetProps](imapiprop-getprops.md) open de l’entrée et la récupération de la propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
    
MAPI_CACHE_ONLY
  
> Ouvre une entrée de carnet d’adresses et y accède uniquement à partir du cache. Par exemple, vous pouvez utiliser cet indicateur pour autoriser une application cliente ouvrir la liste d’adresses globale (LAG) en mode exchange mis en cache et accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer le trafic entre le client et le serveur. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.
    
MAPI_DEFERRED_ERRORS 
  
> Permet l’appel aboutisse, potentiellement avant que l’entrée est entièrement ouverte et disponible, ce qui implique que les appels ultérieurs à l’entrée de renvoyer une erreur.
    
MAPI_GAL_ONLY
  
> Utiliser uniquement la liste d’adresses globale pour effectuer la résolution de noms. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.
    
  > [!NOTE]
  > _ulFlags_ MAPI_GAL_ONLY pas peuvent être définis dans le fichier d’en-tête téléchargeables que vous avez actuellement, auquel cas vous pouvez l’ajouter à votre code à l’aide de la valeur suivante : >`#define MAPI_GAL_ONLY (0x00000080)`
  
N' 
  
> Demandes que l’entrée est ouvert en lecture/écriture autorisation. Étant donné que les entrées sont ouvertes avec accès en lecture seule par défaut, les clients ne doivent pas supposer que l’autorisation de lecture/écriture bénéficie même si n’est définie.
    
MAPI_NO_CACHE
  
> N’utilisez pas le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.
    
_lpulObjType_
  
> [out] Pointeur vers le type de l’entrée ouvert.
    
_lppUnk_
  
> [out] Pointeur vers un pointeur vers l’entrée ouvert.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’entrée a été ouvert avec succès.
    
MAPI_E_NO_ACCESS 
  
> Une tentative a été effectuée pour ouvrir une entrée pour lequel l’utilisateur dispose d’autorisations insuffisantes.
    
MAPI_E_NOT_FOUND 
  
> L’entrée représentée par _lpEntryID_ n’existe pas. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L’identificateur d’entrée spécifié dans _lpEntryID_ n’est pas reconnue. Cette valeur est généralement renvoyée si le fournisseur de carnet d’adresses responsable de l’entrée correspondante n’est pas ouvert. 
    
## <a name="remarks"></a>Remarques

Clients et fournisseurs de services appellent la méthode **IAddrBook::OpenEntry** pour ouvrir une entrée de carnet d’adresses. MAPI transfère l’appel vers le fournisseur de carnet d’adresse appropriée, en fonction de la structure [MAPIUID](mapiuid.md) incluse dans l’identificateur d’entrée passé dans le paramètre _lpEntryID_ . Le fournisseur de carnet d’adresses ouvre l’entrée en lecture seule, sauf si l’indicateur n’ou MAPI_BEST_ACCESS dans le paramètre _ulFlags_ est défini. Toutefois, ces indicateurs sont des suggestions. Si le fournisseur de carnet d’adresses n’autorise pas la modification de l’entrée demandée, il renvoie MAPI_E_NO_ACCESS. 
  
Le paramètre _lpInterface_ indique l’interface qui doit être utilisé pour accéder à l’entrée ouverte. Passage de NULL dans _lpInterface_ indique l’interface MAPI standard pour ce type d’entrée doit être utilisé. Étant donné que le fournisseur de carnet d’adresses peut retourner une interface différente de celle suggérée par le paramètre _lpInterface_ , l’appelant doit vérifier la valeur renvoyée dans le paramètre _lpulObjType_ pour déterminer si le type d’objet retourné est ce qui était attendu. Si le type d’objet n’est pas du type attendu, l’appelant peut effectuer un cast le paramètre _lppUnk_ à un type qui est plus approprié. 
  
## <a name="see-also"></a>Voir aussi

- [IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

