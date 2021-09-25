---
title: IABLogonPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IABLogon.PrepareRecips
api_type:
- COM
ms.assetid: 3c1845ea-e291-4855-9afd-51d2c64d7e85
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a7a9459a1b3eb83540db9ab11e0bb01e7e6cf9de
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584485"
---
# <a name="iablogonpreparerecips"></a>IABLogon::PrepareRecips

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Prépare une liste de destinataires pour une utilisation ultérieure par le système de messagerie.
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Paramètres

_ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type du texte dans les chaînes renvoyées. L’indicateur suivant peut être définie :
    
  - MAPI_CACHE_ONLY : utilisez uniquement le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms. Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d’ouvrir la liste d’adresses globale (LAL) en mode Exchange mis en cache et d’accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer de trafic entre le client et le serveur. Cet indicateur est pris en charge uniquement par le Exchange de carnet d’adresses.
    
_lpPropTagArray_
  
> [in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriétés qui indiquent les propriétés qui nécessitent une mise à jour, le cas contraire. Le  _paramètre lpPropTagArray_ peut être NULL. 
    
_lpRecipList_
  
> [in] Pointeur vers une structure [ADRLIST](adrlist.md) qui contient la liste des destinataires. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La liste des destinataires a été préparée avec succès.
    
MAPI_E_NOT_FOUND 
  
> Un ou plusieurs destinataires dans le  _paramètre lpRecipList_ n’existent pas. 
    
## <a name="return-value"></a>Valeur renvoyée

Un client appelle la méthode MAPI [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) pour modifier ou réorganiser un ensemble de propriétés pour un ou plusieurs destinataires. Les destinataires peuvent ou non faire partie de la liste des destinataires d’un message sortant. MAPI transfère cet appel vers la méthode **IABLogon::P repareRecips** d’un fournisseur de carnet d’adresses. 
  
**IABLogon::P repareRecips** effectue quatre tâches principales : 
  
- Garantit que tous les destinataires de la liste d’adresses pointés par le paramètre  _lpRecipList_ ont un identificateur d’entrée à long terme. 
    
- Garantit que tous les destinataires ont les propriétés spécifiées dans le tableau des valeurs de propriétés pointées par _le paramètre lpPropTagArray._ 
    
- Garantit que les propriétés du tableau de valeurs de propriétés apparaissent avant les autres propriétés qui existaient avant l’appel.
    
- Garantit que l’ordre des propriétés dans la structure [ADRENTRY](adrentry.md) de chaque destinataire dans la structure **ADRLIST** est le même que dans le tableau de valeurs des propriétés. 
    
La structure **ADRENTRY** dans le  _paramètre lpRecipList_ contient une structure **ADRENTRY** pour chaque destinataire. Chaque structure **ADRENTRY** contient un tableau de structures [SPropValue](spropvalue.md) pour décrire les propriétés du destinataire. Lorsque **IABLogon::P repareRecips** renvoie, le tableau de structure **SPropValue** pour chaque destinataire inclut les propriétés de  _lpPropTagArray_ suivies des autres propriétés pour le destinataire. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

L’implémentation **d’IABLogon::P repareRecips** implique de placer les propriétés dans un ordre spécifique, de récupérer les valeurs des propriétés et de convertir les identificateurs d’entrée à court terme en identificateurs d’entrée à long terme. Les propriétés qui sont demandées dans le paramètre _lpPropTagArray_ doivent se trouver au début du tableau de valeurs de propriétés associé à la structure **ADRENTRY** de chaque destinataire dans le paramètre _lpRecipList._ Si les valeurs de ces propriétés n’existent pas, ouvrez l’utilisateur de messagerie ou la liste de distribution associé à l’aide de son identificateur d’entrée et récupérez les valeurs de propriété manquantes. 
  
Allouez chaque structure **SPropValue** transmise dans  _lpRecipList_ séparément afin que les structures soient libérées individuellement. Si vous devez allouer de l’espace supplémentaire à une structure **SPropValue,** par exemple, pour stocker les données d’une propriété de chaîne, utilisez la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) pour allouer de l’espace supplémentaire au tableau de valeurs de propriété complète. Utilisez la [fonction MAPIFreeBuffer](mapifreebuffer.md) pour libérer le tableau de valeurs de propriété d’origine, puis utilisez la [fonction MAPIAllocateMore](mapiallocatemore.md) pour allouer toute mémoire supplémentaire requise. 
  
Pour **implémenter IABLogon::P repareRecips,** utilisez la procédure suivante :
  
1. Recherchez des entrées _dans le paramètre lpPropTagArray._ Si le tableau de valeurs de propriétés est vide, il n’y a aucun travail à faire. Renvoyer une valeur de réussite. 
    
2. Traiter chaque destinataire dans _le paramètre lpRecipList._ Il existe un membre de structure **ADRENTRY** pour chaque destinataire dans la liste. Ignorez les types de destinataires suivants : 
    
   - Destinataires sans identificateur d’entrée dans le membre **rgPropVals** de leur structure **ADRENTRY** (c’est-à-dire, destinataires non résolus). 
    
   - Destinataires avec un identificateur d’entrée qui n’appartient pas à votre fournisseur. Ces destinataires sont transmis à un autre fournisseur de carnet d’adresses.
    
3. Ouvrez le destinataire et récupérez les propriétés qui sont déjà définies pour le destinataire.
    
4. Fusionnez le tableau de valeurs de propriétés spécifié dans  _lpRecipList_ avec le tableau de propriétés renvoyé par **GetProps**. Si la même propriété se produit dans les deux tableaux de propriétés, utilisez la valeur de  _lpRecipList_.
    
5. Si le tableau de valeurs de propriété  _lpRecipList_ est suffisamment grand pour contenir toutes les propriétés nécessaires, remplacez-le simplement par le tableau fusionné. Si le tableau de valeurs de propriété  _lpRecipList_ n’est pas assez grand, remplacez-le par un tableau nouvellement alloué. Assurez-vous que le nouveau tableau a une valeur mise à jour dans chacun de ses membres **cValues.** 
    
6. Si vous ne reconnaissez pas une ou plusieurs propriétés dans le paramètre  _lpPropTagArray,_ définissez le type de propriété dans la structure **ADRENTRY** du destinataire sur PT_ERROR et la valeur de la propriété sur MAPI_E_NOT_FOUND ou sur une autre valeur qui donne une raison plus spécifique de l’indisponibilité de la propriété. Pour plus d’informations PT_ERROR, voir [Types de propriétés.](property-types.md)
    
> [!NOTE]
> Ne réaffectez jamais la structure **ADRLIST** transmise dans **IABLogon::P repareRecips** ou modifiez son nombre d’entrées. 
  
## <a name="see-also"></a>Voir aussi

- [ADRLIST](adrlist.md)
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [Propriété canonique PidTagEntryId](pidtagentryid-canonical-property.md)
- [SPropValue](spropvalue.md)
- [IABLogon : IUnknown](iablogoniunknown.md)

