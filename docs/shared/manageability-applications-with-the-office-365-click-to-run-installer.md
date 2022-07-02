---
title: Intégration d’applications de facilité de gestion à Microsoft 365 Apps programme d’installation démarrer en un clic
manager: lindalu
ms.date: 03/22/2022
ms.audience: ITPro
ms.localizationpriority: medium
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Découvrez comment intégrer le programme d’installation Microsoft 365 Apps Démarrer en un clic à une solution de gestion logicielle.
ms.openlocfilehash: c841b0f6cd147ee621c53c2308413168d9fbd4e0
ms.sourcegitcommit: b9eed77e21325860cef74e4fb8b86adcc247bc09
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2022
ms.locfileid: "66608427"
---
# <a name="integrating-manageability-applications-with-microsoft-365-apps-click-to-run-installer"></a>Intégration d’applications de facilité de gestion à Microsoft 365 Apps programme d’installation démarrer en un clic

Découvrez comment intégrer le programme d’installation Microsoft 365 Apps Démarrer en un clic à une solution de gestion logicielle.
  
Le programme d’installation Microsoft 365 Apps Démarrer en un clic fournit une interface COM qui permet aux professionnels de l’informatique et aux solutions de gestion des logiciels de contrôler par programmation la gestion des mises à jour. Cette interface fournit des fonctionnalités de gestion supplémentaires au-delà de ce qui est fourni par l’outil de déploiement Office.
  
> [!NOTE]
> Cet article s’applique aux applications Office qui utilisent le programme d’installation Démarrer en un clic.
  
## <a name="integrating-with-the-click-to-run"></a>Intégration à l’exécution en un clic

Pour utiliser cette interface, une application de gestion appelle l’interface COM et appelle les API exposées qui communiquent directement avec le service d’installation Démarrer en un clic.
  
> [!NOTE]
> Le programme d’installation Office Démarrer en un clic peut être exécuté à partir de la ligne de commande avec des paramètres qui peuvent contrôler le comportement, comme indiqué dans [l’outil de déploiement Office pour démarrer en un clic](/DeployOffice/overview-office-deployment-tool).
  
**Voici un diagramme conceptuel de l’interface COM**

![Diagramme de l’utilisation de l’interface COM sur le programme d’installation d’Office Démarrer en un clic.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagramme montrant l’utilisation de l’interface COM sur le programme d’installation Démarrer en un clic d’Office")
  
Le programme d’installation Microsoft 365 Apps Démarrer en un clic implémente une interface COM, **IUpdateNotify** inscrite **auprès** de CLSID CLSID_UpdateNotifyObject.
  
Cette interface peut être appelée comme suit :
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

L’appel réussit uniquement si l’appelant s’exécute sous des privilèges élevés, car le programme d’installation Démarrer en un clic doit être exécuté avec des privilèges élevés.
  
**L’interface COM IUpdateNotify** expose trois fonctions asynchrones responsables de la validation des commandes et des paramètres et de la planification de l’exécution avec le service d’installation Démarrer en un clic.
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

Une méthode forth, **Status**, peut être utilisée pour obtenir des informations sur l’état de la dernière commande exécutée ou l’état de la commande en cours d’exécution (par exemple, réussite, échec, codes d’erreur détaillés).
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

Il existe quatre états dans lesquels le service d’installation « Démarrer en un clic » peut se trouver pendant son cycle de vie, au cours duquel les méthodes **IUpdateNotify** peuvent être appelées ; Redémarrage, inactivité, téléchargement et application.
  
**Voici le diagramme de l’ordinateur d’état de l’interface COM**

![Diagramme d’état pour l’interface COM.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Diagramme d’état pour l’interface COM")
  
> [!NOTE]
> **Redémarrage** : lorsque l’ordinateur démarre, le service de programme d’installation « Démarrer en un clic » n’est pas disponible pendant un certain temps. Un appel réussi à la méthode Status après un redémarrage retourne eUPDATE_UNKNOWN.
  
**Inactif:** Lorsque le programme d’installation Démarrer en un clic est dans un état inactif, vous pouvez appeler :
  
- **Appliquer** : installez le contenu précédemment téléchargé.

- **Cancel** : Renvoie `0x800000e`, « Une méthode a été appelée à un moment inattendu ».

- **Téléchargement** : télécharge le nouveau contenu sur le client pour une installation ultérieure.

- **État** : renvoie le résultat de la dernière action terminée, ou un message d’erreur si l’action s’est terminée en échec. S’il n’existe aucune action précédente, **l’état** retourne `eUPDATE_UNKNOWN`.

**Téléchargement:** Lorsque le programme d’installation Démarrer en un clic est dans l’état de téléchargement, vous pouvez appeler :
  
- **Apply** : retourne un **HRESULT** avec la valeur `0x800000e`, « Une méthode a été appelée à un moment inattendu ».

- **Annuler** : arrête le téléchargement et supprime le contenu partiellement téléchargé.

- **Téléchargement** : renvoie un **HRESULT** avec la valeur `0x800000e`« Une méthode a été appelée à un moment inattendu ».

- **État** : renvoie **DOWNLOAD_WIP** pour indiquer que le travail de téléchargement est en cours.

**Application:** Lorsque le programme d’installation démarrer en un clic est en train d’installer le contenu précédemment téléchargé :
  
- **Apply** : retourne un **HRESULT** avec la valeur `0x800000e`, « Une méthode a été appelée à un moment inattendu ».

- **Annuler** : retourne `0x800000e`, l’action Appliquer ne peut pas être annulée.

- **Téléchargement** : renvoie un **HRESULT** avec la valeur `0x800000e`« Une méthode a été appelée à un moment inattendu ».

- **État** : retourne **APPLY_WIP** pour indiquer que le travail d’application est en cours.

> [!NOTE]
> Étant donné qu’OfficeC2RCOM est un service COM+ et qu’il est chargé dynamiquement, vous devez appeler **CoCreateInstance** chaque fois que vous appelez une méthode sur cette classe pour vous assurer d’obtenir le résultat attendu. Le service COM+ gère la création d’une instance si nécessaire. Quand l’une des méthodes est appelée pour la première fois, COM+ charge l’objet **IUpdateNotify** et l’exécute dans l’une des instances dllhost.exe. Le nouvel objet reste actif pendant environ 3 minutes en mode inactif. Si un appel ultérieur est effectué dans les trois minutes suivant le dernier appel, l’objet **IUpdateNotify** reste chargé et une nouvelle instance n’est pas créée. Si aucun appel n’est effectué dans les trois minutes, l’objet IUpdateNotify est déchargé et un nouvel objet **IUpdateNotify** est créé lors de l’appel suivant.
  
## <a name="click-to-run-installer-com-api-reference-guide"></a>Guide de référence de l’API COM du programme d’installation démarrer en un clic

Dans la documentation de référence de l’API suivante :
  
- Les paramètres sont dans un format de paire clé/valeur séparé par un espace.

- Les paramètres ne respectent pas la casse.

- Pour plus d’informations, consultez [Informations sur les installations Office « Démarrer en un clic » et sur les applications anti-programmes malveillants associées](/office/troubleshoot/office-suite-issues/office-click-to-run-installation).

- Le résumé de l’interface IUpdateNotify2 est maintenant inclus.

### <a name="apply"></a>Appliquer

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a>Paramètres

- _displaylevel_ : **true** pour afficher l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour ; **false** pour masquer l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour. La valeur par défaut est **False**.

- _forceappshutdown_ : **true** pour forcer l’arrêt immédiat des applications Office lorsque l’action **Appliquer** est déclenchée ; **false** pour échouer si des applications Office sont en cours d’exécution. La valeur par défaut est **False**. Pour plus d’informations, consultez [Remarques](#bk_ApplyRemark) .

  Si une application Office est en cours d’exécution lorsque l’action **Appliquer** est déclenchée, l’action **Appliquer** échoue généralement. En passant `forceappshutdown=true` à la méthode **Apply** , le service **OfficeClickToRun** arrête immédiatement les applications et applique la mise à jour. Dans ce cas, l’utilisateur peut subir une perte de données.

#### <a name="return-results"></a>Retourner les résultats

|**Résultat**|**Description**|
|:-----|:-----|
|**S_OK** <br/> |L’action a été envoyée avec succès au service Démarrer en un clic pour exécution. |
|**E_ACCESSDENIED** <br/> |L’appelant ne s’exécute pas avec des privilèges élevés. |
|**E_INVALIDARG** <br/> |Des paramètres non valides ont été passés. |
|**E_ILLEGAL_METHOD_CALL** <br/> |L’action n’est pas autorisée pour l’instant. Pour plus d’informations, consultez [Remarques](#bk_ApplyRemark) . |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a>Remarques

- Si une application Office est en cours d’exécution lorsque l’action **Appliquer** est déclenchée, l’action **Appliquer** échoue. En passant `forceappshutdown=true` à la méthode **Apply** , le service **OfficeClickToRun** arrête immédiatement toutes les applications Office en cours d’exécution et applique la mise à jour. L’utilisateur peut rencontrer des données, car il n’est pas invité à enregistrer les modifications pour ouvrir des documents.

- Cette action ne peut être déclenchée que lorsque l’état COM est l’un des suivants :

  - **eUPDATE_UNKNOWN**

  - **eDOWNLOAD_CANCELLED**

  - **eDOWNLOAD_FAILED**

  - **eDOWNLOAD_SUCCEEDED**

  - **eAPPLY_SUCCEEDED**

  - **eAPPLY_FAILED**

- Si vous appelez la méthode **Apply** sans télécharger de contenu précédemment, la méthode **Apply** signale **succeeded** car elle n’a détecté aucune application et a terminé le processus **Apply** avec succès.

### <a name="cancel"></a>Annuler

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a>Retourner les résultats

|**Résultat**|**Description**|
|:-----|:-----|
|S_OK  <br/> |L’action a été envoyée au service Démarrer en un clic pour exécution. |
|E_ILLEGAL_METHOD_CALL  <br/> |L’action n’est pas autorisée pour l’instant. Pour plus d’informations, consultez la section [Notes](#bk_CancelRemarks)  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a>Remarques

- Cette méthode ne peut être déclenchée que lorsque l’ID d’état COM **eDOWNLOAD_WIP**. Il tente d’annuler l’action de téléchargement actuelle. L’état COM passe à **eDOWNLOAD_CANCELLING** et finit par passer à **eDOWNLOAD_CANCELED**. L’état COM retourne **E_ILLEGAL_METHOD_CALL** s’il est déclenché à un autre moment.

### <a name="download"></a>Télécharger

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a>Paramètres

- _displaylevel_ : **true** pour afficher l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour ; **false** pour masquer l’état de l’installation, y compris les erreurs, pendant le processus de mise à jour. La valeur par défaut est **False**.
- _updatebaseurl_ : URL vers la source de téléchargement secondaire.
- _updatetoversion_ : version vers qui mettre à jour Office. Définissez ce paramètre si vous souhaitez mettre à jour vers une version antérieure à la version actuellement installée.
- _downloadsource_ : CLSID de l’implémentation **IBackgroundCopyManager** personnalisée (gestionnaire BITS).
- _contentid_ : identifie le contenu à télécharger à partir du serveur de contenu via le gestionnaire BITS personnalisé. Cette valeur est transmise via l’interface BITS à des fins d’interprétation.

#### <a name="return-results"></a>Retourner les résultats

|**Résultat**|**Description**|
|:-----|:-----|
|**S_OK** <br/> |L’action a été envoyée avec succès au service Démarrer en un clic pour exécution. |
|**E_ACCESSDENIED** <br/> |L’appelant ne s’exécute pas avec des privilèges élevés. |
|**E_INVALIDARG** <br/> |Des paramètres non valides ont été passés. |
|**E_ILLEGAL_METHOD_CALL** <br/> |L’action n’est pas autorisée pour l’instant. Pour plus d’informations, consultez [Remarques](#bk_DownloadRemark) . |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a>Remarques

- Vous devez spécifier _downloadsource_ et _contentid_ en tant que paire. Si ce n’est pas le cas, la méthode **Download** retourne une erreur **E_INVALIDARG** .

- Si _downloadsource_, _contentid_ et _updatebaseurl_ sont fournis, _updatebaseurl_ est ignoré.

- Cette action ne peut être déclenchée que lorsque l’état COM est l’un des suivants :

  - **eUPDATE_UNKNOWN**

  - **eDOWNLOAD_CANCELLED**

  - **eDOWNLOAD_FAILED**

  - **eDOWNLOAD_SUCCEEDED**

  - **eAPPLY_SUCCEEDED**

  - **eAPPLY_FAILED**

- Si vous appelez la méthode **Apply** sans contenu précédemment téléchargé, la méthode **Apply** signale **succeeded** car elle n’a détecté aucune application et a terminé le processus **Apply** avec succès.

#### <a name="examples"></a>Exemples

- Pour télécharger le contenu à partir du gestionnaire BITS personnalisé : Appelez la fonction **download()** en passant les paramètres suivants :

  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- Pour télécharger le contenu à partir du réseau de distribution de contenu Office (CDN) : appelez la fonction **download()** sans spécifier les paramètres _downloadsource_, _contentid_ ou _updatebaseurl_ .

- Pour télécharger le contenu à partir d’un emplacement personnalisé : Appelez la fonction **download()** en passant le paramètre suivant :

  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a>État

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a>Paramètres

|**Paramètre**|**Description**|
|:-----|:-----|
| _pUpdateStatusReport_ <br/> |Pointeur vers une structure UPDATE_STATUS_REPORT. |

#### <a name="return-results"></a>Retourner les résultats

|**Résultat**|**Description**|
|:-----|:-----|
|**S_OK** <br/> |La méthode **Status** retourne toujours ce résultat. Inspectez la `UPDATE_STATUS_RESULT` structure pour connaître l’état de l’action actuelle. |

#### <a name="remarks"></a>Remarques

- Le champ d’état de l’action `UPDATE_STATUS_REPORT` contient l’état de l’action actuelle. L’une des valeurs d’état suivantes est retournée :

  ```cpp
  typedef enum _UPDATE_STATUS
  {
  eUPDATE_UNKNOWN = 0,
  eDOWNLOAD_PENDING,
  eDOWNLOAD_WIP,
  eDOWNLOAD_CANCELLING,
  eDOWNLOAD_CANCELLED,
  eDOWNLOAD_FAILED,
  eDOWNLOAD_SUCCEEDED,
  eAPPLY_PENDING,
  eAPPLY_WIP,
  eAPPLY_SUCCEEDED,
  eAPPLY_FAILED,
  } UPDATE_STATUS;
  
  ```

- Si la dernière commande a provoqué une erreur, le champ d’erreur contient `UPDATE_STATUS_REPORT` des informations détaillées sur l’erreur. Deux types de codes d’erreur sont retournés à partir de la méthode **Status** .

- Si l’erreur est inférieure à , l’erreur est l’un des codes d’erreur prédéfinis suivants `UPDATE_ERROR_CODE::eUNKNOWN`:

  ```cpp
  typedef enum _UPDATE_ERROR_CODE
  {
  eOK = 0,
  eFAILED_UNEXPECTED,
  eTRIGGER_DISABLED,
  ePIPELINE_IN_USE,
  eFAILED_STOP_C2RSERVICE,
  eFAILED_GET_CLIENTUPDATEFOLDER,
  eFAILED_LOCK_PACKAGE_TO_UPDATE,
  eFAILED_CREATE_STREAM_SESSION,
  eFAILED_PUBLISH_WORKING_CONFIGURATION,
  eFAILED_DOWNLOAD_UPGRADE_PACKAGE,
  eFAILED_APPLY_UPGRADE_PACKAGE,
  eFAILED_INITIALIZE_RSOD,
  eFAILED_PUBLISH_RSOD,
  // Keep this one as the last
  eUNKNOWN
  } UPDATE_ERROR_CODE;
  
  ```

  Si le code d’erreur de retour est supérieur `UPDATE_ERROR_CODE::eUNKNOWN` au **HRESULT** d’un appel de fonction ayant échoué. Pour extraire la soustraction `UPDATE_ERROR_CODE::eUNKNOWN` HRESULT de la valeur retournée dans le champ d’erreur du `UPDATE_STATUS_REPORT`.

  Vous pouvez afficher la liste complète des valeurs d’état et d’erreur en inspectant la bibliothèque de types **IUpdateNotify** incorporée dans OfficeC2RCom.dll.

- Le champ contentid est utilisé pour les appels à **l’état** après le lancement du **téléchargement** et retourne l’ID de contenu qui a été passé à l’appel **de téléchargement** . Il est recommandé d’initialiser ce champ sur **null** avant d’appeler la méthode **Status** , puis de vérifier la valeur une fois **l’état** retourné. Si la valeur est toujours **null**, cela signifie qu’il n’y a aucun contentid à retourner. Si la valeur n’est pas **null**, vous devez la libérer avec un appel à **SysFreeString()**. Voici un extrait de code montrant comment appeler **Status** après **le téléchargement**.

  ```cpp
  std::wstring contentID;
  UPDATE_STATUS_REPORT statusReport;
  statusReport.status = eUPDATE_UNKNOWN;
  statusReport.error = eOK;
  statusReport.contentid = NULL;
  hr = p->Status(&statusReport);
  if (statusReport.contentid != NULL)
  {
  contentID = statusReport.contentid;
  SysFreeString(statusReport.contentid);
  }
  wprintf(L"ContentID: %s, Status: %d, LastError: %d", contentID.c_str(), statusReport.status, statusReport.error);
  
  ```

### <a name="summary-of-iupdatenotify2-interface"></a>Résumé de l’interface IUpdateNotify2

À partir de la version [16.0.8208.6352], nous avons ajouté une nouvelle interface **IUpdateNotify2** .
  
- CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DFE}

- Cette interface a également hébergé l’interface IUpdateNotify d’origine pour assurer la compatibilité descendante. Ce qui signifie que si vous utilisez cette interface, vous avez accès à toutes les méthodes fournies dans l’interface **UpdateNotifyObject** .

- Nouvelles méthodes ajoutées à IUpdateNotify2 :

  - **HRESULT** GetBlockingApps([out] BSTR \* AppsList). Obtenir la liste des applications bloquantes des mises à jour. Cet appel renverra les applications Office en cours d’exécution, ce qui empêchera le processus de mise à jour de continuer.

  - **HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR * OfficeData). Obtenir les données de déploiement d’Office.

- Si vous souhaitez utiliser les nouvelles méthodes, vous devez vous assurer que :

  - Votre version C2R est plus récente que la build ci-dessus (\>= build de duplication de juin).

  - Utilisez UpdateNotifyObject2, au lieu de **UpdateNotifyObject** pour appeler **CoCreateInstance**.

Si vous n’utilisez aucune des nouvelles méthodes, vous n’avez rien à changer. Toutes les méthodes existantes fonctionnent exactement de la même façon qu’auparavant.
  
## <a name="implementing-the-bits-interface"></a>Implémentation de l’interface BITS

Le service BITS ( [Background Intelligent Transfer Service](/windows/win32/bits/background-intelligent-transfer-service-portal) ) est un service fourni par Microsoft pour transférer des fichiers entre un client et un serveur. BITS est l’un des canaux que le programme d’installation Démarrer en un clic d’Office peut utiliser pour télécharger du contenu. Par défaut, le programme d’installation Microsoft 365 Apps Démarrer en un clic utilise l’implémentation intégrée de BITS de Windows pour télécharger le contenu à partir du CDN.
  
En fournissant une implémentation BITS personnalisée à la méthode **download()** de l’interface **IUpdateNotify** , votre logiciel de gestion peut contrôler où et comment le client télécharge le contenu. Une interface BITS personnalisée est utile lorsque vous fournissez un canal de distribution de contenu personnalisé autre que les canaux intégrés « Démarrer en un clic », tels que le CDN, les serveurs IIS ou les partages de fichiers.
  
La configuration minimale requise pour qu’une interface BITS personnalisée fonctionne avec le service Office C2R est la suivante :
  
- Pour **IBackgroundCopyManager** :

  ```cpp
  HRESULT _stdcall CreateJob(
                      [in] LPWSTR DisplayName, 
                      [in] BG_JOB_TYPE Type, 
                      [out] GUID* pJobId, 
                      [out] IBackgroundCopyJob** ppJob)
  HRESULT _stdcall GetJob(
                      [in] GUID* jobID, 
                      [out] IBackgroundCopyJob** ppJob)
  HRESULT _stdcall EnumJobs(
                      [in] unsigned long dwFlags, 
                      [out] IEnumBackgroundCopyJobs** ppenum)
  
  ```

- Pour **IBackgroundCopyJob** :

  ```cpp
  HRESULT _stdcall AddFile(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName)
  HRESULT _stdcall Resume()
  HRESULT _stdcall Complete()
  HRESULT _stdcall Cancel();
  HRESULT _stdcall GetState([out] BG_JOB_STATE* pVal);
  HRESULT GetProgress( [out] BG_JOB_PROGRESS *pProgress);
  
  ```

- Pour **IBackgroundCopyJob3** :

  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- Pour les fonctions et `AddFileWithRanges` les `Addfile` fonctions, l’URL distante est au format suivant :

  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - cmbits est codé en dur et signifie BITS personnalisé.

  - _\<contentid\>_ est le paramètre _contentid_ de la méthode **Download().**

  - _\<relative path to target file\>_ fournit l’emplacement et le nom du fichier à télécharger.

    Par exemple, si vous avez fourni un _contentid_ de `f732af58-5d86-4299-abe9-7595c35136ef` la méthode **Download()** et qu’Office C2R souhaite télécharger le fichier cab de version, tel que `v32.cab` le fichier, il appelle **AddFile()** avec les éléments suivants :`RemoteUrl`

  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- Pour **IBackgroundCopyError** :

  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- Pour **IBackgroundCopyFile** :

  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```

## <a name="automating-content-staging"></a>Automatisation de la préproduction de contenu

Les administrateurs informatiques peuvent choisir d’activer les clients de bureau pour recevoir automatiquement les mises à jour lorsqu’ils sont disponibles directement à partir du CDN ou ils peuvent choisir de contrôler le déploiement des mises à jour disponibles à partir des canaux de mise à jour à l’aide de l’outil de déploiement Office ou du point de terminaison Microsoft Configuration Manager.
  
Le service prend en charge la possibilité pour les outils de gestion de reconnaître et d’automatiser le téléchargement du contenu lorsque des mises à jour sont mises à disposition.
  
**L’image suivante est une vue d’ensemble du téléchargement d’une image personnalisée**

![Diagramme de l’utilisation de l’interface COM sur le programme d’installation d’Office Démarrer en un clic.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagramme montrant l’utilisation de l’interface COM sur le programme d’installation Démarrer en un clic d’Office")
  
### <a name="overview-of-downloading-a-custom-image"></a>Vue d’ensemble du téléchargement d’une image personnalisée
  
Dans le diagramme précédent, vous voyez qu’une nouvelle image Microsoft 365 Apps est disponible sur le CDN. En plus de l’image Microsoft 365 Apps, une API est disponible avec les informations nécessaires pour permettre aux logiciels de gestion de créer directement des images personnalisées en remplaçant la nécessité d’utiliser l’outil de déploiement Office.

Une entreprise configure son WSUS pour synchroniser les mises à jour Microsoft 365 Apps. Ces mises à jour ne contiennent pas la charge utile réelle de l’image, mais permettent au logiciel de gestion de reconnaître quand un nouveau contenu est disponible. Le logiciel de gestion peut ensuite lire les métadonnées de mise à jour Microsoft 365 Apps pour comprendre à quelle version d’Office la mise à jour s’applique.

Si la mise à jour est applicable, le logiciel de gestion peut utiliser le contenu CDN et la liste de fichiers pour créer l’image personnalisée et la stocker dans l’emplacement du partage de fichiers qu’elle est configurée pour l’utiliser.
  
### <a name="using-the-microsoft-365-apps-file-list-api"></a>Utilisation de l’API de liste de fichiers Microsoft 365 Apps

L’API de liste de fichiers Microsoft 365 Apps est utilisée pour récupérer les noms des fichiers nécessaires à une mise à jour Microsoft 365 Apps particulière.

Requête HTTP

GET <https://config.office.com/api/filelist>

N’indiquez pas le corps de la demande pour cette méthode.

Aucune autorisation n’est requise pour appeler cette API.

Paramètres facultatifs de la requête

|**Nom**|**Description**|
|:-----|:-----|
| Canal <br/>| Spécifie le nom du canal  <br/> Facultatif : valeur par défaut « SemiAnnual » <br/> Valeurs prises en charge </DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element.md> |
| version <br/>| Spécifie la version de mise à jour <br/> Facultatif : correspond par défaut à la dernière version disponible pour le canal spécifié |
| Arc <br/>| Spécifie l’architecture du client <br/> Facultatif : la valeur par défaut est « x64 » <br/> Valeurs prises en charge : x64, x86 |
| Couvercle <br/>| Spécifie les fichiers de langue à inclure <br/> Facultatif : la valeur par défaut est none <br/> Pour spécifier plusieurs langues, incluez un paramètre de requête lid pour chaque langue <br/> Utilisez le format d’identificateur de langue, par exemple. 'en-us', 'fr-fr' |
| alllanguages <br/>| Spécifie d’inclure tous les fichiers linguistiques <br/> Facultatif : valeur par défaut false |

**Réponse HTTP**

Si elle réussit, cette méthode renvoie un code de réponse 200 OK et une collection d’objets de fichier dans le corps de la réponse.

Pour créer une image, procédez comme suit :

1. Appelez l’API, en fournissant les paramètres de requête appropriés pour le canal, la version et l’architecture de la mise à jour qui vous intéresse.
Remarque : les objets de fichier avec l’attribut « lcid » : « 0 » sont des fichiers indépendants de la langue et doivent être inclus dans l’image.
2. Construisez une image locale du CDN en itérant à travers les objets de fichier et en copiant les fichiers CDN, tout en créant la structure de dossiers spécifiée par l’attribut « relativePath » défini pour chacun des objets de fichier.

L’exemple suivant récupère la liste des fichiers pour le canal actuel et la version 16.0.4229.1004 pour 64 bits et inclut les fichiers de langue Français et anglais.

```http
Get https://config.office.com/api/filelist?Channel=Current&Version=16.0.4229.1004&Arch=x64&Lid=fr-fr&Lid=en-US
```

### <a name="hash-verification-of-dat-files"></a>Vérification du hachage des fichiers .dat

Les outils de création d’images peuvent vérifier l’intégrité des fichiers .dat téléchargés en comparant une valeur de hachage calculée avec la valeur de hachage fournie associée à chacun des fichiers .dat. Voici un exemple d’objet de fichier qui spécifie des valeurs hashLocation et hashAlgorithm :
  
```xml
{
  "url": "https://officecdn.microsoft.com/pr/7ffbc6bf-bc32-4f92-8982-f9dd17fd3114/office/data/16.0.1234.1001/stream.x64.x-none.dat",
  "name": "stream.x64.x-none.dat",
  "relativePath": "/office/data/16.0.1234.1001/",
  "hashLocation": "s640.cab/stream.x64.x-none.hash",
  "hashAlgorithm": "Sha256",
  "lcid": "0"
},
```

- **L’attribut hashLocation** spécifie l’emplacement du chemin d’accès relatif de .cab fichier qui contient la valeur de hachage. Construisez l’emplacement du fichier de hachage en concaténant l’URL + relativePath + hashLocation. Dans l’exemple suivant, l’emplacement stream.x64.bg-bg.hash serait :

  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- **L’attribut hashAlgorithm** spécifie l’algorithme de hachage utilisé.

  Pour valider l’intégrité du fichier stream.x64.bg-bg.dat, ouvrez le stream.x64.bg-bg.hash et lisez la valeur HASH qui est la première ligne de texte dans le fichier de hachage. Comparez cette valeur à la valeur de hachage calculée (à l’aide de l’algorithme de hachage spécifié) pour vérifier l’intégrité du fichier .dat téléchargé.

  L’exemple suivant montre le code C# pour lire le hachage.

  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="microsoft-365-apps-updates"></a>Microsoft 365 Apps Mises à jour

Tous les Microsoft 365 Apps Mises à jour sont publiés dans le [catalogue Microsoft Update](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client).
  
Microsoft 365 Apps Mises à jour permettre aux logiciels de gestion de traiter Microsoft 365 Apps Mises à jour d’une manière très similaire à toute autre mise à jour WU à une exception près ; les mises à jour clientes ne contiennent pas de charge utile réelle. Le Microsoft 365 Apps Mises à jour ne doit pas être installé sur des clients, mais plutôt utilisé pour déclencher les flux de travail avec le logiciel de facilité de gestion remplaçant la commande d’installation par le mécanisme d’installation COM indiqué ci-dessus.

**La figure suivante montre un diagramme du flux de travail de mise à jour du client Office 365.**

![Diagramme de flux de travail pour les mises à jour du client O365PP.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Diagramme de flux de travail pour les mises à jour du client O365PP")
  
Chaque Microsoft 365 Apps mise à jour publiée inclut les métadonnées relatives à la mise à jour. Ces métadonnées incluent un paramètre appelé MoreInfoUrl qui peut être utilisé pour dériver l’appel d’API à l’API de liste de fichiers pour cette mise à jour spécifique.

Dans l’exemple suivant, l’API de liste de fichiers est incorporée dans MoreInfoURL et commence par « ServicePath= »

<https://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml>& ServicePath=<https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True>
  
### <a name="additional-metadata-for-automating-content-staging"></a>Métadonnées supplémentaires pour l’automatisation de la préproduction de contenu

**API de découverte de mise en production**
  
L’API de découverte de version Microsoft 365 Apps est utilisée pour récupérer les détails de chacune des mises à jour publiées sur le CDN, ainsi que les noms de canaux et autres attributs de canal.

Requête HTTP

```http
GET [https://config.office.com/api/filelist/channels](https://clients.config.office.net/releases/v1.0/OfficeReleases) 
```

N’indiquez pas le corps de la demande pour cette méthode.

Aucune autorisation n’est requise pour appeler cette API.

Réponse HTTP

Si elle réussit, cette méthode renvoie un code de réponse 200 OK et une collection d’objets de fichier dans le corps de la réponse.

**API de références SKU**
  
L’API de références SKU retourne des informations utiles pour déterminer les produits disponibles pour le déploiement et la maintenance à partir du CDN Office, ainsi que différentes options pour chacune d’elles.

Requête HTTP

```http
GET [https://config.office.com/api/filelist/skus](https://config.office.com/api/filelist/skus) 
```

N’indiquez pas le corps de la demande pour cette méthode.

Aucune autorisation n’est requise pour appeler cette API.

Réponse HTTP

Si elle réussit, cette méthode renvoie un code de réponse 200 OK et une collection d’objets de fichier dans le corps de la réponse.
