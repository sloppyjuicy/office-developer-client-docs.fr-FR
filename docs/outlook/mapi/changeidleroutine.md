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
  
Modifie une partie ou l'ensemble des caractéristiques d'une routine inactive basée sur [FNIDLE](fnidle.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
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

## <a name="parameters"></a>Paramètres

_FTG_
  
> dans Balise de fonction qui identifie la routine inactive. 
    
_pfnIdle_
  
> dans Pointeur vers la routine inactive. 
    
_pvIdleParam_
  
> dans Pointeur vers un nouveau bloc de mémoire que l'implémentation d'appel alloue pour la routine inactive. 
    
_priIdle_
  
> dans Valeur représentant une nouvelle priorité pour la routine inactive. Les priorités possibles pour les routines définies par l'implémentation sont supérieures ou inférieures à zéro, mais pas à zéro. La valeur zéro est réservée à un événement utilisateur tel qu'un clic de souris ou un message WM_PAINT. Les valeurs supérieures à zéro représentent des priorités pour les tâches d'arrière-plan dont la priorité est supérieure à celle des événements utilisateur et qui sont distribuées dans le cadre de la boucle Windows message Pump standard. Les valeurs inférieures à zéro représentent des priorités pour les tâches inactives qui s'exécutent uniquement pendant la durée d'inactivité de la pompe de messages. Exemples de priorités: 1 pour l'envoi de premier plan, 1 pour l'insertion de caractères de modification de l'alimentation et 3 pour le téléchargement de nouveaux messages.
    
_csecIdle_
  
> dans Une nouvelle heure, en centièmes de seconde, à appliquer à la routine inactive. La signification de la valeur de l'heure initiale varie en fonction de ce qui est passé dans le paramètre _iroIdle_ . Il peut s'agir des éléments suivants: 
    
  - Période minimale d'inaction de l'utilisateur qui doit s'écouler avant que le moteur inactif MAPI appelle la routine inactive pour la première fois, si l'indicateur FIROWAIT est défini dans _iroIdle_. Une fois ce délai passé, le moteur inactif peut appeler la routine inactive aussi souvent que nécessaire. 
    
  - Intervalle minimal entre les appels à la routine inactive, si l'indicateur FIROINTERVAL est défini dans _iroIdle_. 
    
_iroIdle_
  
> dans Masque de des indicateurs indiquant les nouvelles options d'appel de la routine inactive. Exactement l'un des indicateurs suivants doit être défini:
    
  - FIROINTERVAL: le temps spécifié par le paramètre _csecIdle_ est l'intervalle minimal entre les appels successifs de la routine inactive. 
      
  - FIROONCEONLY: obsolète. Ne pas utiliser. 
      
  - FIROPERBLOCK: obsolète. Ne pas utiliser. 
      
  - FIROWAIT: le temps spécifié par le paramètre _csecIdle_ est la période minimale d'inaction de l'utilisateur qui doit s'écouler avant que le moteur d'inactivité MAPI appelle la routine inactive pour la première fois. Une fois ce délai passé, le moteur inactif peut appeler la routine inactive aussi souvent que nécessaire. 
    
_ircIdle_
  
> dans Masque de des indicateurs utilisé pour indiquer les modifications à apporter à la routine inactive. Les indicateurs suivants peuvent être définis dans n'importe quelle combinaison:
    
  - FIRCCSEC: modification de l'heure associée à la routine inactive, c'est-à-dire un changement indiqué par la valeur transmise dans le paramètre _csecIdle_ . 
      
  - FIRCIRO: modification des options de la routine inactive, c'est-à-dire un changement indiqué par la valeur transmise dans le paramètre _iroIdle_ . 
      
  - FIRCPFN: modification du pointeur de routine inactive, c'est-à-dire un changement indiqué par la valeur transmise dans le paramètre _pfnIdle_ . 
      
  - FIRCPRI: modification de la priorité de la routine inactive, c'est-à-dire d'une modification indiquée par la valeur transmise dans le paramètre _priIdle_ . 
      
  - FIRCPV: modification du bloc de mémoire de la routine inactive, c'est-à-dire un changement indiqué par la valeur transmise dans le paramètre _pvIdleParam_ . 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Les fonctions suivantes concernent le moteur inactif MAPI et les routines inactives basées sur le prototype de fonction [FNIDLE](fnidle.md) : 
  
|**Fonction de routine inactive**|**Usage**|
|:-----|:-----|
|**ChangeIdleRoutine** <br/> |Modifie les caractéristiques d'une routine inactive enregistrée.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Supprime une routine inactive inscrite du système MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Désactive ou réactive une routine inactive enregistrée sans la supprimer du système MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Ajoute une routine inactive au système MAPI, avec ou sans l'activer.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Arrête le moteur d'inactivité MAPI pour l'application appelante.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialise le moteur d'inactivité MAPI pour l'application appelante.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**et **EnableIdleRoutine** prennent comme paramètre d'entrée la balise de fonction renvoyée par **FtgRegisterIdleRoutine**. 
  
Lorsque toutes les tâches de premier plan de la plate-forme deviennent inactives, le moteur inactif MAPI appelle la routine inactive de priorité la plus élevée qui est prête à s'exécuter. Il n'existe aucune garantie d'appel de commande entre les routines inactives de la même priorité. 
  

