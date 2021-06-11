---
title: ChangeIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ChangeIdleRoutine
api_type:
- HeaderDef
ms.assetid: 0a24fe3b-a1ef-4748-b3b3-3bf747473c9d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: cfec9356a866c79b687497c3af007c046a20a75e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418266"
---
# <a name="changeidleroutine"></a>ChangeIdleRoutine

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Modifie une partie ou l’ensemble des caractéristiques d’une routine [d’inactivité basée sur FNIDLE.](fnidle.md) 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
VOID ChangeIdleRoutine(
  FTG ftg,
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle,
  USHORT ircIdle
);
```

## <a name="parameters"></a>Parameters

_ftg_
  
> [in] Balise de fonction qui identifie la routine inactive. 
    
_pfnIdle_
  
> [in] Pointeur vers la routine inactive. 
    
_pvIdleParam_
  
> [in] Pointeur vers un nouveau bloc de mémoire que l’implémentation d’appel alloue à la routine inactive. 
    
_priIdle_
  
> [in] Valeur représentant une nouvelle priorité pour la routine inactive. Les priorités possibles pour les routines définies par l’implémentation sont supérieure ou inférieure à zéro, mais pas à zéro. La valeur zéro est réservée à un événement utilisateur tel qu’un clic de souris ou un WM_PAINT message. Les valeurs supérieures à zéro représentent les priorités des tâches en arrière-plan dont la priorité est plus élevée que les événements utilisateur et qui sont envoyées dans le cadre de la boucle de boucle de Windows de message standard. Les valeurs inférieures à zéro représentent les priorités des tâches inactives qui s’exécutent uniquement pendant les périodes d’inactivité de message. Voici quelques exemples de priorités : 1 pour l’envoi au premier plan, 1 pour l’insertion de caractères avec modification d’alimentation et 3 pour le téléchargement de nouveaux messages.
    
_csecIdle_
  
> [in] Nouvelle heure, en centièmes de seconde, à appliquer à la routine inactive. La signification de la valeur d’heure initiale varie en fonction de ce qui est transmis dans le _paramètre iroIdle._ Il peut s’y trouver : 
    
  - Période minimale d’inaction de l’utilisateur qui doit s’écoulée avant que le moteur inactif MAPI appelle la routine d’inactivité pour la première fois, si l’indicateur FIROWAIT est définie en  _iroIdle_. Une fois ce délai passé, le moteur inactif peut appeler la routine d’inactivité aussi souvent que nécessaire. 
    
  - Intervalle minimal entre les appels à la routine inactive, si l’indicateur FIROINTERVAL est définie dans  _iroIdle_. 
    
_iroIdle_
  
> [in] Masque de bits d’indicateurs indiquant de nouvelles options pour appeler la routine inactive. Vous devez définir exactement l’un des indicateurs suivants :
    
  - FIROINTERVAL : l’heure spécifiée par le paramètre  _csecIdle_ est l’intervalle minimal entre les appels successifs à la routine inactive. 
      
  - FIROONCEONLY : Obsolète. Ne pas utiliser. 
      
  - FIROPERBLOCK : Obsolète. Ne pas utiliser. 
      
  - FIROWAIT : le temps spécifié par le paramètre  _csecIdle_ est la période minimale d’inaction de l’utilisateur qui doit s’écoulée avant que le moteur inactif MAPI appelle la routine d’inactivité pour la première fois. Une fois ce délai passé, le moteur inactif peut appeler la routine d’inactivité aussi souvent que nécessaire. 
    
_Ideidle_
  
> [in] Masque de bits d’indicateurs utilisé pour indiquer les modifications à apporter à la routine inactive. Les indicateurs suivants peuvent être définies dans n’importe quelle combinaison :
    
  - FIRCCSEC : modification de l’heure associée à la routine d’inactivité, c’est-à-dire une modification indiquée par la valeur passée dans le paramètre _csecIdle._ 
      
  - FIRCIRO : modification des options de la routine inactive, c’est-à-dire une modification indiquée par la valeur transmise dans le _paramètre iroIdle._ 
      
  - FIRCPFN : modification du pointeur de routine inactif, c’est-à-dire une modification indiquée par la valeur transmise dans le _paramètre pfnIdle._ 
      
  - FIRCPRI : modification de la priorité de la routine inactive, c’est-à-dire une modification indiquée par la valeur transmise dans le _paramètre priIdle._ 
      
  - FIRCPV : modification du bloc mémoire de la routine inactive, c’est-à-dire une modification indiquée par la valeur transmise dans le paramètre _pvIdleParam._ 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Les fonctions suivantes traitent du moteur inactif MAPI et des routines inactives basées sur le prototype de fonction [FNIDLE](fnidle.md) : 
  
|**Fonction de routine inactive**|**Utilisation**|
|:-----|:-----|
|**ChangeIdleRoutine** <br/> |Modifie les caractéristiques d’une routine inactive inscrite.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Supprime une routine d’inactivité enregistrée du système MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Désactive ou réactive une routine d’inactivité enregistrée sans la supprimer du système MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Ajoute une routine inactive au système MAPI, avec ou sans l’activer.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Arrête le moteur d’inactivité MAPI pour l’application à l’appel.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialise le moteur d’inactivité MAPI pour l’application à l’appel.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine** et **EnableIdleRoutine** prennent comme paramètre d’entrée la balise de fonction renvoyée par **FtgRegisterIdleRoutine**. 
  
Lorsque toutes les tâches au premier plan de la plateforme deviennent inactives, le moteur inactif MAPI appelle la routine d’inactivité la plus prioritaire prête à être exécuté. Il n’existe aucune garantie d’appel de l’ordre parmi les routines inactives de la même priorité. 
  

