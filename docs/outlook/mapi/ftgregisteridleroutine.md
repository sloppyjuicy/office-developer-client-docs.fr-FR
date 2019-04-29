---
title: FtgRegisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtgRegisterIdleRoutine
api_type:
- COM
ms.assetid: 8d9557ba-7919-42c6-9e2f-f10214437d53
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b45b80f09efbd4f05aabc2c868d5bd8eb5fa4cce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418520"
---
# <a name="ftgregisteridleroutine"></a>FtgRegisterIdleRoutine

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajoute une routine inactive basée sur la fonction [FNIDLE](fnidle.md) au système MAPI. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
FTG FtgRegisterIdleRoutine(
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle
);
```

## <a name="parameters"></a>Paramètres

_pfnIdle_
  
> dans Pointeur vers la routine inactive. 
    
_pvIdleParam_
  
> dans Pointeur vers un bloc de mémoire que le moteur inactif doit transmettre en tant que paramètre à la routine inactive lorsqu'il l'appelle. 
    
_priIdle_
  
> dans Priorité initiale de la routine inactive. Les priorités possibles pour les routines définies par l'implémentation sont supérieures ou inférieures à zéro, mais pas à zéro. La priorité zéro est réservée à un événement utilisateur tel qu'un clic de souris ou un message WM_PAINT. Les priorités supérieures à zéro représentent les tâches en arrière-plan dont la priorité est supérieure à celle des événements utilisateur et qui sont distribuées dans le cadre de la boucle Windows message Pump standard. Les priorités inférieures à zéro représentent des tâches inactives qui s'exécutent uniquement pendant la durée d'inactivité de la pompe de messages. Voici des exemples de priorités: 1 pour l'envoi de premier plan, 2 pour l'insertion de caractères de modification de l'alimentation et 3 pour le téléchargement de nouveaux messages.
    
_csecIdle_
  
> dans Valeur de l'heure initiale, en centièmes de seconde, à utiliser pour spécifier les paramètres de routine inactive. La signification de la valeur de l'heure initiale varie en fonction de ce qui est passé dans le paramètre _iroIdle_ . La signification peut être l'une des suivantes: 
    
  - Période minimale d'inaction de l'utilisateur qui doit s'écouler avant que le moteur inactif MAPI appelle la routine inactive pour la première fois, si l'indicateur FIROWAIT est défini dans _iroIdle_. Une fois ce délai passé, le moteur inactif peut appeler la routine inactive aussi souvent que nécessaire. 
    
  - Intervalle minimal entre les appels à la routine inactive, si l'indicateur FIROINTERVAL est défini dans _iroIdle_. 
    
_iroIdle_
  
> dans Masque de réinitialisation des indicateurs utilisés pour définir les options initiales de la routine inactive. Les indicateurs suivants peuvent être définis:
    
  FIRONOADJUSTMENT
    
  > Utilisez cet indicateur pour spécifier que le minuteur de la routine inactive ne doit pas être ajusté en mode veille ou reprise. Le comportement par défaut sans cet indicateur est que le temps de sommeil est exclu lors du calcul du temps écoulé. Si FIRONOADJUSTMENT est transmis, la durée de veille est incluse lors du calcul du temps écoulé.
      
  FIRODISABLED
    
  > La routine inactive doit être désactivée lors de l'inscription. L'action par défaut consiste à activer la routine inactive lorsque **FtgRegisterIdleRoutine** l'enregistre. 
      
  FIROINTERVAL 
    
  > Le temps spécifié par le paramètre _csecIdle_ est l'intervalle minimal entre les appels successifs de la routine inactive. 
      
  FIROONCEONLY 
    
  > Obsolète. Ne pas utiliser. 
      
  FIROPERBLOCK 
    
  > Obsolète. Ne pas utiliser. 
      
  FIROWAIT 
    
  > Le temps spécifié par le paramètre _csecIdle_ est la période minimale d'inaction de l'utilisateur qui doit s'écouler avant que le moteur d'inactivité MAPI appelle la routine inactive pour la première fois. Une fois ce délai passé, le moteur inactif peut appeler la routine inactive aussi souvent que nécessaire. 
    
## <a name="return-value"></a>Valeur renvoyée

La fonction **FtgRegisterIdleRoutine** renvoie une balise de fonction identifiant la routine inactive qui a été ajoutée au système MAPI. Si **FtgRegisterIdleRoutine** ne parvient pas à enregistrer la routine inactive pour l'application cliente ou le fournisseur de services, par exemple en raison de problèmes de mémoire, elle renvoie la valeur null. 
  
## <a name="remarks"></a>Remarques

Les fonctions suivantes concernent le moteur inactif MAPI et les routines inactives basées sur le prototype de fonction [FNIDLE](fnidle.md) . 
  
|**Fonction de routine inactive**|**Usage**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Modifie les caractéristiques d'une routine inactive enregistrée.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Supprime une routine inactive inscrite du système MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Désactive ou réactive une routine inactive enregistrée sans la supprimer du système MAPI.  <br/> |
|**FtgRegisterIdleRoutine** <br/> |Ajoute une routine inactive au système MAPI, avec ou sans l'activer.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Arrête le moteur d'inactivité MAPI pour l'application appelante.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialise le moteur d'inactivité MAPI pour l'application appelante.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**et **EnableIdleRoutine** prennent comme paramètre d'entrée la balise de fonction renvoyée par **FtgRegisterIdleRoutine**. 
  
Lorsque toutes les tâches de premier plan de la plate-forme deviennent inactives, le moteur inactif MAPI appelle la routine inactive de priorité la plus élevée qui est prête à s'exécuter. Il n'existe aucune garantie d'appel de commande entre les routines inactives de la même priorité. 
  
Voici un exemple d'utilisation de l'indicateur FIRONOADJUSTMENT dans le paramètre _iroIdle_ . 
  
1. Enregistrer une routine inactive avec un délai de 5 minutes.
    
2. Mettre en veille/mettre l'ordinateur en veille après 1 minute (4 minutes restantes sur le minuteur).
    
3. Reprendre l'ordinateur 10 minutes plus tard.
    
Le comportement par défaut, sans FIRONOADJUSTMENT, est que vous devez attendre 4 minutes supplémentaires pour l'exécution de votre routine. Autrement dit, votre minuteur a été ajusté pour permettre pendant combien de temps l'ordinateur était en mode veille. Toutefois, si vous transmettez FIRONOADJUSTMENT, votre routine inactive s'exécutera immédiatement car plus de 5 minutes de temps réel se sont écoulées.
  

