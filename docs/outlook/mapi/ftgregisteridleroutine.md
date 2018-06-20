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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0d3f24c41f2cfbd499d92e050c74da904dd4c377
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783385"
---
# <a name="ftgregisteridleroutine"></a>FtgRegisterIdleRoutine

**S’applique à**: Outlook 
  
Ajoute une routine [FNIDLE](fnidle.md) fonction inactive au système MAPI. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
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
  
> [in] Pointeur vers la routine inactif. 
    
_pvIdleParam_
  
> [in] Pointeur vers un bloc de mémoire que le moteur d’inactivité doit transmettre en tant que paramètre à la routine inactive lorsqu’il l’appelle. 
    
_priIdle_
  
> [in] La priorité initiale de la routine d’inactivité. Priorités possibles pour les routines défini par l’implémentation sont supérieur ou inférieur à zéro, mais pas de zéro. La priorité de zéro est réservée pour un événement utilisateur comme un clic de souris ou d’un message WM_PAINT. Supérieure à zéro des priorités représentent des tâches en arrière-plan qui ont une priorité plus élevée que les événements de l’utilisateur et sont exécutés dans le cadre de la boucle de pompe de message Windows standard. Priorités inférieur à zéro représente les tâches inactives uniquement être exécutées pendant la durée d’inactivité pompe message. Exemples de priorités sont les suivantes : 1 pour l’envoi de premier plan, 2 pour l’insertion de caractère power-modifier et 3 pour le téléchargement de nouveaux messages.
    
_csecIdle_
  
> [in] La valeur de la première fois, dans centième de seconde, à utiliser pour spécifier les paramètres de routine inactifs. La signification de la valeur d’heure initiale varie, selon ce qui est passé dans le paramètre _iroIdle_ . La signification peut être une des options suivantes : 
    
  - La durée minimale d’inaction utilisateur qui doit s’écouler avant l’interface MAPI moteur inactif appelle la routine inactive pour la première fois, si l’indicateur FIROWAIT est défini dans _iroIdle_. Une fois ce délai, le moteur d’inactivité peut appeler la routine inactive aussi souvent que nécessaire. 
    
  - L’intervalle minimal entre les appels à la routine inactive, si l’indicateur FIROINTERVAL est défini dans _iroIdle_. 
    
_iroIdle_
  
> [in] Masque de bits d’indicateurs utilisés pour définir les options initiales de la routine d’inactivité. Les indicateurs suivants peuvent être définis :
    
  FIRONOADJUSTMENT
    
  > Utilisez cet indicateur pour spécifier que l’horloge de routine ne doit pas être ajustée pour la mise en veille ou de reprendre. Le comportement par défaut sans cet indicateur est que la durée de veille est exclue lors du calcul du temps écoulé. Si FIRONOADJUSTMENT est passée la durée de veille est incluse lors du calcul de temps écoulé.
      
  FIRODISABLED
    
  > La routine d’inactivité doit être désactivée lorsque enregistré. L’action par défaut consiste à activer la routine inactive lorsque **FtgRegisterIdleRoutine** inscrit. 
      
  FIROINTERVAL 
    
  > L’heure spécifiée par le paramètre _csecIdle_ est l’intervalle entre les appels successifs de la routine d’inactivité minimale. 
      
  FIROONCEONLY 
    
  > Obsolète. Ne pas utiliser.  
      
  FIROPERBLOCK 
    
  > Obsolète. Ne pas utiliser.  
      
  FIROWAIT 
    
  > L’heure spécifiée par le paramètre _csecIdle_ est la durée minimale d’inaction utilisateur qui doit s’écouler avant que le moteur d’inactivité MAPI appelle la routine inactive pour la première fois. Une fois ce délai, le moteur d’inactivité peut appeler la routine inactive aussi souvent que nécessaire. 
    
## <a name="return-value"></a>Valeur renvoy�e

La fonction **FtgRegisterIdleRoutine** renvoie une balise de fonction qui identifie la routine d’inactivité qui a été ajoutée au système MAPI. Si **FtgRegisterIdleRoutine** ne peut pas enregistrer la routine d’inactivité pour l’application cliente ou d’un fournisseur de services, par exemple en raison de problèmes de mémoire, elle renvoie la valeur NULL. 
  
## <a name="remarks"></a>Remarques

Les fonctions suivantes traitent avec le moteur d’inactivité MAPI et routines inactifs basées sur le prototype de fonction [FNIDLE](fnidle.md) . 
  
|**Fonction de routine inactive**|**Utilisation**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Modifie les caractéristiques d’une routine d’inactivité inscrit.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Supprime une routine d’inactivité inscrit dans le système MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Active ou désactive réactive une routine d’inactivité inscrit sans la supprimer à partir du système MAPI.  <br/> |
|**FtgRegisterIdleRoutine** <br/> |Ajoute une routine inactive au système MAPI, avec ou sans l’activer.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Arrête le moteur d’inactivité MAPI pour l’application appelante.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialise le moteur d’inactivité MAPI pour l’application appelante.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**et **EnableIdleRoutine** prennent comme paramètre d’entrée de la balise de fonction retournée par **FtgRegisterIdleRoutine**. 
  
Lorsque toutes les tâches de premier plan pour la plateforme sont inactives, le moteur d’inactivité MAPI appelle la routine d’inactivité priorité la plus élevée qui est prête à exécuter. Il n’existe aucune garantie de l’appel de commande entre inactifs routines de même priorité. 
  
Voici un exemple d’utilisation de l’indicateur FIRONOADJUSTMENT dans le paramètre _iroIdle_ . 
  
1. Enregistrer une routine inactive avec un délai de 5 minutes.
    
2. Mise en veille prolongée/veille l’ordinateur après 1 minute (4 minutes à gauche de l’horloge).
    
3. Redémarrez l’ordinateur 10 minutes plus tard.
    
Le comportement par défaut, sans FIRONOADJUSTMENT, est que vous devrez attendre 4 minutes pour exécuter votre routine. Autrement dit, le minuteur a été ajustée pour permettre la durée pendant laquelle l’ordinateur était en veille. Toutefois, si vous transmettez FIRONOADJUSTMENT votre routine inactif exécutera immédiatement car plus de 5 minutes de temps réel se sont écoulées.
  

