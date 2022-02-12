---
title: FtgRegisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FtgRegisterIdleRoutine
api_type:
- COM
ms.assetid: 8d9557ba-7919-42c6-9e2f-f10214437d53
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b2f925b3104a71858515394740512ca4dbf094dd
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62780075"
---
# <a name="ftgregisteridleroutine"></a>FtgRegisterIdleRoutine

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajoute une [routine d’inactivité basée sur la fonction FNIDLE](fnidle.md) au système MAPI. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
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
  
> [in] Pointeur vers la routine inactive. 
    
_pvIdleParam_
  
> [in] Pointeur vers un bloc de mémoire que le moteur inactif doit transmettre en tant que paramètre à la routine inactive lorsqu’il l’appelle. 
    
_priIdle_
  
> [in] Priorité initiale de la routine inactive. Les priorités possibles pour les routines définies par l’implémentation sont supérieure ou inférieure à zéro, mais pas à zéro. La priorité zéro est réservée à un événement utilisateur tel qu’un clic de souris ou un WM_PAINT message. Les priorités supérieures à zéro représentent des tâches en arrière-plan dont la priorité est plus élevée que les événements utilisateur et qui sont envoyées dans le cadre de la boucle d’Windows de message standard. Les priorités inférieures à zéro représentent les tâches inactives qui s’exécutent uniquement pendant la période d’inactivité des messages. Voici quelques exemples de priorités : 1 pour l’envoi au premier plan, 2 pour l’insertion de caractères avec modification d’alimentation et 3 pour le téléchargement de nouveaux messages.
    
_csecIdle_
  
> [in] Valeur d’heure initiale, en centièmes de seconde, à utiliser pour spécifier les paramètres de routine inactifs. La signification de la valeur d’heure initiale varie en fonction de ce qui est transmis dans le _paramètre iroIdle_ . La signification peut être l’une des suivantes : 
    
  - Période minimale d’inaction de l’utilisateur qui doit s’écoulée avant que le moteur inactif MAPI appelle la routine d’inactivité pour la première fois, si l’indicateur FIROWAIT est définie en  _iroIdle_. Une fois ce délai passé, le moteur inactif peut appeler la routine d’inactivité aussi souvent que nécessaire. 
    
  - Intervalle minimal entre les appels à la routine inactive, si l’indicateur FIROINTERVAL est définie dans  _iroIdle_. 
    
_iroIdle_
  
> [in] Masque de bits des indicateurs utilisés pour définir les options initiales de la routine inactive. Les indicateurs suivants peuvent être définies :
    
  FIRONOADJUSTMENT
    
  > Utilisez cet indicateur pour spécifier que le temps d’inactivité de routine ne doit pas être ajusté pour la veille ou la reprise. Le comportement par défaut sans cet indicateur est que le temps de veille est exclu lors du calcul du temps écoulé. Si FIRONOADJUSTMENT est passé, le temps de veille est inclus lors du calcul du temps écoulé.
      
  FIRODISABLED
    
  > La routine inactive doit être désactivée lorsqu’elle est inscrite. L’action par défaut consiste à activer la routine inactive lorsque **FtgRegisterIdleRoutine** l’inscrit. 
      
  FIROINTERVAL 
    
  > Le temps spécifié par le  _paramètre csecIdle_ est l’intervalle minimal entre les appels successifs à la routine inactive. 
      
  FIROONCEONLY 
    
  > Obsolète. Ne pas utiliser.  
      
  FIROPERBLOCK 
    
  > Obsolète. Ne pas utiliser.  
      
  FIROWAIT 
    
  > Le temps spécifié par le paramètre  _csecIdle_ est la période minimale d’inaction de l’utilisateur qui doit s’écoulée avant que le moteur inactif MAPI appelle la routine d’inactivité pour la première fois. Une fois ce délai passé, le moteur inactif peut appeler la routine d’inactivité aussi souvent que nécessaire. 
    
## <a name="return-value"></a>Valeur renvoyée

La **fonction FtgRegisterIdleRoutine** renvoie une balise de fonction identifiant la routine inactive qui a été ajoutée au système MAPI. Si **FtgRegisterIdleRoutine** ne peut pas inscrire la routine d’inactivité pour l’application cliente ou le fournisseur de services, par exemple en raison de problèmes de mémoire, elle renvoie la valeur NULL. 
  
## <a name="remarks"></a>Remarques

Les fonctions suivantes traitent du moteur inactif MAPI et des routines inactives basées sur le prototype de fonction [FNIDLE](fnidle.md) . 
  
|**Fonction de routine inactive**|**Utilisation**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Modifie les caractéristiques d’une routine d’inactivité inscrite. |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Supprime une routine d’inactivité enregistrée du système MAPI. |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Désactive ou réactive une routine d’inactivité enregistrée sans la supprimer du système MAPI. |
|**FtgRegisterIdleRoutine** <br/> |Ajoute une routine inactive au système MAPI, avec ou sans l’activer. |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Arrête le moteur d’inactivité MAPI pour l’application à l’appel. |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialise le moteur d’inactivité MAPI pour l’application à l’appel. |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine** et **EnableIdleRoutine** prennent comme paramètre d’entrée la balise de fonction renvoyée par **FtgRegisterIdleRoutine**. 
  
Lorsque toutes les tâches au premier plan de la plateforme deviennent inactives, le moteur inactif MAPI appelle la routine d’inactivité la plus prioritaire prête à être exécuté. Il n’existe aucune garantie d’appel d’ordre parmi les routines inactives de la même priorité. 
  
Voici un exemple d’utilisation de l’indicateur FIRONOADJUSTMENT dans le _paramètre iroIdle_ . 
  
1. Inscrivez une routine inactive avec un délai de 5 minutes.
    
2. Mettre en veille prolongée/mettre en veille prolongée l’ordinateur après 1 minute (4 minutes à gauche sur le minuteur).
    
3. Reprendront l’ordinateur 10 minutes plus tard.
    
Le comportement par défaut, sans FIRONOADJUSTMENT, est que vous devez toujours attendre 4 minutes supplémentaires pour que votre routine s’exécute. Autrement dit, votre système de temps a été ajusté pour autoriser la durée de veille de l’ordinateur. Toutefois, si vous passez FIRONOADJUSTMENT, votre routine d’inactivité s’exécutera immédiatement car plus de 5 minutes de temps réel se sont écoulées.
  

