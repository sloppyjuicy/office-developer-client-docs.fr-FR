---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Initialise un objet IOlkApptRebaser à utiliser lors de la relocalisation des rendez-vous dans les calendriers Outlook.
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317611"
---
# <a name="hrcreateapptrebaser"></a>HrCreateApptRebaser

Initialise un objet [IOlkApptRebaser](iolkapptrebaser.md) à utiliser lors de la relocalisation des rendez-vous dans les calendriers Outlook. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |tzmovelib. h  <br/> |
|Implémenté par :  <br/> |tzmovelib. dll  <br/> |
|Appelé par :  <br/> |Applications clientes MAPI  <br/> |
|Type de pointeur:  <br/> |**LPHRCREATEAPPTREBASER** <br/> |
|Point d'entrée de DLL:  <br/> |**HrCreateApptRebaser @ 44** <br/> |
   
```cpp
HRESULT HrCreateApptRebaser(  
    ULONG ulFlags, 
    IMAPISession *pSession, 
    IMsgStore *pCalendarMsgStore, 
    IMAPIFolder *pCalendarFolder, 
    LPCWSTR pwszUpdatePrefix, 
    const FILETIME *pftInstallDateUTC, 
    LONG lExpansionDepth, 
    const TZDEFINITION *pTZTo, 
    const TZDEFINITION *pTZMissing, 
    MAPIERROR **ppError, 
    IOlkApptRebaser **ppApptRebase); 

```

## <a name="parameters"></a>Paramètres

_ulFlags_
  
> [in] Obligatoire. Masque de des indicateurs utilisés pour contrôler la manière dont la relocalisation est effectuée. Les indicateurs suivants peuvent être définis et définis dans tzmovelib. h:
    
   - **REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** : éléments de rendez-vous dans lesquels l'utilisateur est l'organisateur de la réunion qui est rebasé. Notez que, par défaut, Outlook envoie les mises à jour de réunion à tous les participants de toutes les réunions rebasés. Vous pouvez associer cet indicateur à **REBASE_FLAG_FORCE_NO_EX_UPDATES** ou **REBASE_FLAG_FORCE_NO_UPDATES** pour modifier la façon dont les mises à jour de réunion sont gérées. 
    
   - **REBASE_FLAG_UPDATE_UNMARKED** : mettre à jour les éléments de rendez-vous qui n'ont pas été marqués avec un fuseau horaire. Si cet indicateur est spécifié, la valeur *pTZMissing* est utilisée comme le fuseau horaire dans lequel un élément est créé pour tous les éléments qui n'ont pas de données de fuseau horaire. 
    
   - **REBASE_FLAG_UPDATE_ONLYRECURRING** — mettre à jour uniquement les éléments de rendez-vous périodiques. 
    
   - **REBASE_FLAG_NO_UI** : n'affiche pas d'interface utilisateur, y compris les boîtes de dialogue d'ouverture de session qui s'affichent généralement lors de l'ouverture d'une banque de messages. 
    
   - **REBASE_FLAG_UPDATE_MINIMIZEAPPTS** — ne rebasez pas les éléments de rendez-vous qui se produisent dans le passé. 
    
   - **REBASE_FLAG_FORCE_REBASE** — ne pas vérifier l'organisateur pour les décisions de relocalisation, mais rebaser les éléments de rendez-vous dans lesquels l'utilisateur est un participant. 
    
   - **REBASE_FLAG_FORCE_NO_EX_UPDATES** — envoyer les mises à jour uniquement si l'utilisateur est l'organisateur et si le destinataire n'est pas connecté à un serveur Exchange. 
    
   - **REBASE_FLAG_FORCE_NO_UPDATES** — ne jamais envoyer de mises à jour. 
    
   - **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** — relocaliser uniquement les éléments de rendez-vous uniques créés avant l'application du correctif. 
    
   - **REBASE_FLAG_REPORTING_MODE** : ne rebasez pas réellement les éléments de rendez-vous qui seraient rebasés. 
    
   - **REBASE_FLAG_SEND_RESOURCE_UPDATES** — envoyer des mises à jour de réunion aux ressources. 
    
_pSession_
  
> [in] Obligatoire. Pointeur vers une interface de session MAPI.
    
_pCalendarMsgStore_
  
> [in] Obligatoire. Pointeur vers une banque de messages contenant des éléments de rendez-vous à rebaser.
    
_pCalendarFolder_
  
> [in] Obligatoire. Pointeur vers un dossier de calendrier contenant des éléments de rendez-vous à rebaser.
    
_pwszUpdatePrefix_
  
> [in] Facultatif. Pointeur vers une chaîne contenant le préfixe à ajouter au début des demandes de réunion. Peut être NULL.
    
_pftInstallDateUTC_
  
> [in] Facultatif. Date d'installation du correctif du fuseau horaire. Utilisé uniquement si l'indicateur **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** est défini. 
    
_IExpansionDepth_
  
> [in] Facultatif. Profondeur d'expansion lors de l'extension des listes de distribution pour exclure les destinataires connectés à Exchange Server. Utilisé uniquement si l'indicateur **REBASE_FLAG_FORCE_NO_EX_UPDATES** est défini. 
    
_pTZTo_
  
> [in] Obligatoire. Pointeur vers une structure **TZDEFINITION** décrivant le fuseau horaire à rebaser. **TZDEFINITION** est défini dans tzmovelib. 
    
pTZMissing
  
> [in] Obligatoire. Pointeur vers une structure **TZDEFINITION** décrivant le fuseau horaire à supposer si les informations de fuseau horaire ne sont pas marquées sur un élément. Ne doit pas être NULL, mais utilisé uniquement si l'indicateur **REBASE_FLAG_UPDATE_UNMARKED** est défini. 
    
_ppError_
  
> remarquer Pointeur vers un pointeur vers une structure **MAPIERROR** contenant les informations de version, de composant et de contexte pour l'erreur. Peut être NULL si aucune information d'erreur étendue n'est souhaitée. Gratuit avec [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx). 
    
_ppApptRebase_
  
> remarquer Pointeur vers un pointeur vers l'interface **IOlkApptRebaser** renvoyée. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Remarques

Lors de l'utilisation de [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) pour Rechercher l'adresse de cette fonction dans tzmovelib. dll, spécifiez **HrCreateApptRebaser @ 44** comme nom de procédure. Les indicateurs ne sont pas tous valides les uns avec les autres. 
  
Pour plus d'informations sur les différentes options, voir la section «Glossaire des options de ligne de commande pour l'outil de mise à jour des données de fuseau horaire Outlook» dans l' [article KB 931667: How to address Time Zone Changes by using the Time fuseau Data Update Tool for Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).
  
## <a name="see-also"></a>Voir aussi

- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

