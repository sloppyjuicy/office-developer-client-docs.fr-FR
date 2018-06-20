---
title: FNIDLE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FNIDLE
api_type:
- COM
ms.assetid: f6b31bb4-69dd-43de-b62b-abfa99557641
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bf1a84a1f305580fc9d9085753ab7eb5c62b8aa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783339"
---
# <a name="fnidle"></a>FNIDLE
 
**S’applique à**: Outlook 
  
Définit une routine d’inactive le moteur inactif MAPI appelle régulièrement en fonction de la priorité. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Fonction implémentée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
|Fonction appelée par :  <br/> |MAPI  <br/> |
|Type de pointeur correspondant :  <br/> |PFNIDLE  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Paramètres

 _lpvContext_
  
> [in] Pointeur vers un bloc de mémoire que MAPI passe à la routine inactive chaque fois qu’il l’appelle. Ce pointeur est passé au moteur MAPI inactif dans le paramètre _pvIdleParam_ par [FtgRegisterIdleRoutine](ftgregisteridleroutine.md). Les données dans le bloc de mémoire peuvent fournir le contexte de l’appel de la routine d’inactivité, tels que les objets à utiliser, ou l’état actuel d’une longue opération.
    
## <a name="return-value"></a>Valeur renvoy�e

FALSE 
  
> Une routine inactive avec le prototype **FNIDLE** doit renvoient toujours la valeur FALSE. 
    
## <a name="remarks"></a>Remarques

Les fonctionnalités spécifiques de la routine d’inactivité sont déterminée par l’implémentation des applications de client ou le fournisseur de services. 
  
Le client ou le fournisseur doit limiter la durée d’exécution de chaque état d’une routine d’inactivité. Chaque état doit effectuer une quantité minimale de traitement, mettre à jour l’état actuel dans les données de contexte désignées par _lpvContext_et retourner au moteur de MAPI inactif. 
  
Le client ou le fournisseur doit appeler la fonction MAPI [MAPIInitIdle](mapiinitidle.md) avant qu’il peut enregistrer son propre routine inactif par un appel à la fonction [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) . 
  
Les fonctions suivantes traitent avec le moteur d’inactivité MAPI et routines inactifs basées sur le prototype de fonction FNIDLE : 
  
|**Fonction de routine inactive**|**Utilisation**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Modifie les caractéristiques d’une routine d’inactivité inscrit.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Supprime une routine d’inactivité inscrit dans le système MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Active ou désactive réactive une routine d’inactivité inscrit sans la supprimer à partir du système MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Ajoute une routine inactive au système MAPI, avec ou sans l’activer.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Arrête le moteur d’inactivité MAPI pour l’application appelante.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Initialise le moteur d’inactivité MAPI pour l’application appelante.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**et **EnableIdleRoutine** prennent comme paramètre d’entrée de la balise de fonction retournée par **FtgRegisterIdleRoutine**. 
  
Lorsque toutes les tâches de premier plan pour la plateforme sont inactives, le moteur d’inactivité MAPI appelle la routine d’inactivité priorité la plus élevée qui est prête à exécuter. Il n’existe aucune garantie de l’appel de commande entre inactifs routines de même priorité. 
  

