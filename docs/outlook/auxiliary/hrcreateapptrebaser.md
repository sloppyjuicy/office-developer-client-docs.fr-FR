---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Initialise un objet IOlkApptRebaser pour une utilisation dans le rebasing de rendez-vous dans Outlook calendriers.
ms.openlocfilehash: 8c9b8e2081904f9e37916a13b904d1595fc108a1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592780"
---
# <a name="hrcreateapptrebaser"></a>HrCreateApptRebaser

Initialise un objet [IOlkApptRebaser](iolkapptrebaser.md) à utiliser dans le rebasing de rendez-vous Outlook calendriers. 
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |tzmovelib.h  <br/> |
|Implémenté par :  <br/> |tzmovelib.dll  <br/> |
|Appelé par :  <br/> |Applications clientes MAPI  <br/> |
|Type de pointeur :  <br/> |**LPHRCREATEAPPTREBASER** <br/> |
|Point d’entrée DLL :  <br/> |**HrCreateApptRebaser@44** <br/> |
   
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
  
> [in] Obligatoire. Masque de bits d’indicateurs utilisés pour contrôler la façon dont le rebasing est effectué. Les indicateurs suivants peuvent être définis et définis dans tzmovelib.h :
    
   - **REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** : les éléments de rendez-vous dont l’utilisateur est l’organisateur de la réunion sont rebasenés. Notez que, par défaut, cela Outlook envoyer des mises à jour de réunion à tous les participants d’une réunion en cours de rebase. Vous pouvez combiner cet indicateur avec des REBASE_FLAG_FORCE_NO_EX_UPDATES **ou** **REBASE_FLAG_FORCE_NO_UPDATES** pour modifier la façon dont les mises à jour de réunion sont gérées. 
    
   - **REBASE_FLAG_UPDATE_UNMARKED** : mettre à jour les éléments de rendez-vous qui n’ont pas été marqués avec un fuseau horaire. Si cet indicateur est spécifié, la valeur  *pTZMissing*  est utilisée comme fuseau horaire où un élément est créé pour tous les éléments qui n’ont pas de données de fuseau horaire. 
    
   - **REBASE_FLAG_UPDATE_ONLYRECURRING** — Mettre à jour uniquement les éléments de rendez-vous périodiques. 
    
   - **REBASE_FLAG_NO_UI** : n’affichez aucune interface utilisateur, y compris les boîtes de dialogue d’ouverture de boîte de dialogue généralement affichées lors de l’ouverture d’une magasin de messages. 
    
   - **REBASE_FLAG_UPDATE_MINIMIZEAPPTS** : ne pas rebaser les éléments de rendez-vous qui se produisent dans le passé. 
    
   - **REBASE_FLAG_FORCE_REBASE** : ne recherchez pas les décisions de rebasation dans l’organisateur, mais rebasez les éléments de rendez-vous dans lesquels l’utilisateur est un participant. 
    
   - **REBASE_FLAG_FORCE_NO_EX_UPDATES** : envoyer des mises à jour uniquement si l’utilisateur est l’organisateur et que le destinataire n’est pas connecté à un Exchange Server. 
    
   - **REBASE_FLAG_FORCE_NO_UPDATES** : ne jamais envoyer de mises à jour. 
    
   - **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** : rebaser uniquement les éléments de rendez-vous à instance unique créés avant l’application du correctif. 
    
   - **REBASE_FLAG_REPORTING_MODE** — Ne rebasez pas réellement, signalez simplement les éléments de rendez-vous qui seraient rebasenés. 
    
   - **REBASE_FLAG_SEND_RESOURCE_UPDATES** : envoyer des mises à jour de réunion aux ressources. 
    
_pSession_
  
> [in] Obligatoire. Pointeur vers une interface de session MAPI.
    
_pCalendarMsgStore_
  
> [in] Obligatoire. Pointeur vers une magasin de messages contenant des éléments de rendez-vous à rebaser.
    
_pCalendarFolder_
  
> [in] Obligatoire. Pointeur vers un dossier de calendrier contenant les éléments de rendez-vous à rebaser.
    
_pwszUpdatePrefix_
  
> [in] Facultatif. Pointeur vers une chaîne contenant le préfixe à préfixer sur les demandes de réunion. Peut être NULL.
    
_pftInstallDateUTC_
  
> [in] Facultatif. Date d’installation du correctif de fuseau horaire. Utilisé uniquement si **l’REBASE_FLAG_ONLY_CREATED_PRE_PATCH** est définie. 
    
_IExpansionDepth_
  
> [in] Facultatif. Profondeur d’expansion lors de l’extension des listes de distribution pour exclure les destinataires connectés Exchange Server. Utilisé uniquement si **l’REBASE_FLAG_FORCE_NO_EX_UPDATES** est définie. 
    
_pTZTo_
  
> [in] Obligatoire. Pointeur vers une structure **TZDEFINITION** décrivant le fuseau horaire à rebaser. **TZDEFINITION est** défini dans tzmovelib. 
    
pTZMissing
  
> [in] Obligatoire. Pointeur vers une structure **TZDEFINITION** décrivant le fuseau horaire à prendre en charge si les informations de fuseau horaire ne sont pas estampillées sur un élément. Ne doit pas être NULL, mais utilisé uniquement si **l’REBASE_FLAG_UPDATE_UNMARKED** est définie. 
    
_ppError_
  
> [out] Pointeur vers un pointeur vers une structure **MAPIERROR** contenant des informations de version, de composant et de contexte pour l’erreur. Peut être NULL si aucune information d’erreur étendue n’est souhaitée. Gratuit avec [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx). 
    
_ppApptRebase_
  
> [out] Pointeur vers un pointeur vers l’interface **IOlkApptRebaser** renvoyée. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.
  
## <a name="remarks"></a>Remarques

Lorsque vous [utilisez GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) pour rechercher l’adresse de cette fonction dans tzmovelib.dll, spécifiez **HrCreateApptRebaser@44** comme nom de procédure. Tous les indicateurs ne sont pas valides en combinaison les uns avec les autres. 
  
Pour plus d’informations sur les différentes options, voir la section « Glossaire des options de ligne de commande pour l’outil de mise à jour des données de fuseau horaire Outlook » dans la base de données 931667 : Comment résoudre les changements de fuseau horaire à l’aide de l’outil de mise à jour des données de fuseau horaire [pour Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).
  
## <a name="see-also"></a>Voir aussi

- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

