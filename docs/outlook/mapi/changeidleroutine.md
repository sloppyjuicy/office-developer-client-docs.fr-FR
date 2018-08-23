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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 49682007946a4c5dda3800751deaebcc0e1e5740
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579451"
---
# <a name="changeidleroutine"></a>ChangeIdleRoutine

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Modifie certaines ou toutes les caractéristiques d’une routine d’inactivité [FNIDLE](fnidle.md) en fonction de. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
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

_ftg_
  
> [in] Balise de fonction qui identifie la routine inactive. 
    
_pfnIdle_
  
> [in] Pointeur vers la routine inactive. 
    
_pvIdleParam_
  
> [in] Pointeur vers un nouveau bloc de mémoire qui alloue de l’implémentation d’appel de la routine d’inactivité. 
    
_priIdle_
  
> [in] Valeur qui représente une nouvelle priorité de la routine d’inactivité. Priorités possibles pour les routines défini par l’implémentation sont supérieur ou inférieur à zéro, mais pas de zéro. La valeur zéro est réservée pour un événement utilisateur comme un clic de souris ou d’un message WM_PAINT. Les valeurs supérieures à zéro représentent des priorités pour les tâches en arrière-plan qui ont une priorité plus élevée que les événements de l’utilisateur et sont exécutés dans le cadre de la boucle de pompe de message Windows standard. Les valeurs inférieures à zéro représentent des priorités pour les tâches inactives qui s’exécutent uniquement pendant les temps morts durant copie du message. Exemples de priorités : 1 pour l’envoi de premier plan, 1 pour l’insertion de caractère power-modifier et 3 pour le téléchargement de nouveaux messages.
    
_csecIdle_
  
> [in] Une nouvelle date dans centième de seconde, à appliquer à la routine inactive. La signification de la valeur d’heure initiale varie, selon ce qui est passé dans le paramètre _iroIdle_ . Il peut être : 
    
  - La durée minimale d’inaction utilisateur qui doit s’écouler avant l’interface MAPI moteur inactif appelle la routine inactive pour la première fois, si l’indicateur FIROWAIT est défini dans _iroIdle_. Une fois ce délai, le moteur d’inactivité peut appeler la routine inactive aussi souvent que nécessaire. 
    
  - L’intervalle minimal entre les appels à la routine inactive, si l’indicateur FIROINTERVAL est défini dans _iroIdle_. 
    
_iroIdle_
  
> [in] Masque de bits d’indicateurs indiquant les nouvelles options pour appeler la routine inactive. Un des indicateurs suivants doit être défini :
    
  - FIROINTERVAL : L’heure spécifiée par le paramètre _csecIdle_ est l’intervalle entre les appels successifs de la routine d’inactivité minimale. 
      
  - FIROONCEONLY : obsolète. Ne pas utiliser. 
      
  - FIROPERBLOCK : obsolète. Ne pas utiliser. 
      
  - FIROWAIT : L’heure spécifiée par le paramètre _csecIdle_ est la durée minimale d’inaction utilisateur qui doit s’écouler avant que le moteur d’inactivité MAPI appelle la routine inactive pour la première fois. Une fois ce délai, le moteur d’inactivité peut appeler la routine inactive aussi souvent que nécessaire. 
    
_ircIdle_
  
> [in] Masque de bits d’indicateurs utilisés pour indiquer les modifications à apporter à la routine inactive. Les indicateurs suivants peuvent être définis dans n’importe quelle combinaison :
    
  - FIRCCSEC : Une modification apportée à l’heure associée à la routine inactive, c'est-à-dire, une modification indiquée par la valeur transmise au paramètre _csecIdle_ . 
      
  - FIRCIRO : Une modification dans les options de la routine d’inactivité, autrement dit, une modification indiquée par la valeur passée dans le paramètre _iroIdle_ . 
      
  - FIRCPFN : Une modification du pointeur de routine inactif, autrement dit, une modification indiquée par la valeur passée dans le paramètre _pfnIdle_ . 
      
  - FIRCPRI : Une modification apportée à la priorité de la routine d’inactivité, autrement dit, une modification indiquée par la valeur passée dans le paramètre _priIdle_ . 
      
  - FIRCPV : Une modification dans le bloc de mémoire de la routine d’inactivité, autrement dit, une modification indiquée par la valeur passée dans le paramètre _pvIdleParam_ . 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Les fonctions suivantes traitent avec le moteur d’inactivité MAPI et routines inactifs basées sur le prototype de fonction [FNIDLE](fnidle.md) : 
  
|**Fonction de routine inactive**|**Utilisation**|
|:-----|:-----|
|**ChangeIdleRoutine** <br/> |Modifie les caractéristiques d’une routine d’inactivité inscrit.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Supprime une routine d’inactivité inscrit dans le système MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Active ou désactive réactive une routine d’inactivité inscrit sans la supprimer à partir du système MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Ajoute une routine inactive au système MAPI, avec ou sans l’activer.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Arrête le moteur d’inactivité MAPI pour l’application appelante.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialise le moteur d’inactivité MAPI pour l’application appelante.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**et **EnableIdleRoutine** prennent comme paramètre d’entrée de la balise de fonction retournée par **FtgRegisterIdleRoutine**. 
  
Lorsque toutes les tâches de premier plan pour la plateforme sont inactives, le moteur d’inactivité MAPI appelle la routine d’inactivité priorité la plus élevée qui est prête à exécuter. Il n’existe aucune garantie de l’appel de commande entre inactifs routines de même priorité. 
  

