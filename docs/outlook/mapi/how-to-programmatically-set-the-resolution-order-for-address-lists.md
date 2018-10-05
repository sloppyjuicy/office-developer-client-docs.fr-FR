---
title: Définir par programme l’ordre de résolution des listes d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f9559afb-8db1-ce72-3e11-9b3d47bb80b6
description: 'Dernière modification : 06 juillet 2012'
ms.openlocfilehash: 4ca3e9d11a3133236d38ef31b01ecded932e8013
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392916"
---
# <a name="programmatically-set-the-resolution-order-for-address-lists"></a><span data-ttu-id="fdc84-103">Définir par programme l’ordre de résolution des listes d’adresses</span><span class="sxs-lookup"><span data-stu-id="fdc84-103">Programmatically set the resolution order for address lists</span></span>
  
<span data-ttu-id="fdc84-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fdc84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fdc84-105">Cette rubrique contient un exemple de code en langage C++ qui définit par programmation l’ordre des listes d’adresses par les destinataires de courrier électronique messages et les participants dans les demandes de réunion sont résolus.</span><span class="sxs-lookup"><span data-stu-id="fdc84-105">This topic contains a code sample in C++ that programmatically sets the order of address lists by which recipients in email messages and attendees in meeting requests are resolved.</span></span>
  
<span data-ttu-id="fdc84-106">MAPI, chaque profil peut prendre en charge plusieurs listes d’adresses et chaque liste d’adresses réside dans son propre conteneur.</span><span class="sxs-lookup"><span data-stu-id="fdc84-106">In MAPI, each profile can support multiple address lists and each address list resides in its own container.</span></span> <span data-ttu-id="fdc84-107">MAPI prend en charge la méthode **[SetSearchPath](https://support.microsoft.com/kb/292590)** dans l’interface qui vous permet de définir un nouveau chemin d’accès de la recherche dans le profil qui est utilisé pour la résolution de nom.</span><span class="sxs-lookup"><span data-stu-id="fdc84-107">MAPI supports the **[SetSearchPath](https://support.microsoft.com/kb/292590)** method in the interface that allows you to set a new search path in the profile that is used for name resolution.</span></span> <span data-ttu-id="fdc84-108">Pour utiliser la méthode **IAddrBook::SetSearchPath** , que vous aurez définir l’ordre de résolution de votre choix dans un tableau de **[SRowSet](srowset.md)** qui contient les conteneurs des carnets d’adresses pertinents dans l’ordre souhaité, puis spécifiez le tableau comme le *lpSearchPath*  paramètre.</span><span class="sxs-lookup"><span data-stu-id="fdc84-108">To use the **IAddrBook::SetSearchPath** method, you have to define the desired resolution order in a **[SRowSet](srowset.md)** array that holds the containers of the relevant address books in the desired order, and then specify the array as the  *lpSearchPath*  parameter.</span></span> <span data-ttu-id="fdc84-109">La première propriété de chaque entrée dans le tableau **SRowSet** doit être la propriété **[PR_ENTRYID](pidtagentryid-canonical-property.md)** du carnet d’adresses correspondant.</span><span class="sxs-lookup"><span data-stu-id="fdc84-109">The first property for each entry in the **SRowSet** array must be the **[PR_ENTRYID](pidtagentryid-canonical-property.md)** property of the corresponding address book.</span></span> 
  
<span data-ttu-id="fdc84-110">L’exemple de code définit l’ordre de résolution dans les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="fdc84-110">The code sample sets the resolution order in the following steps:</span></span>
  
1. <span data-ttu-id="fdc84-111">Initialise `numANR` et le nombre de conteneurs en correspondance et spécifie les noms et l’ordre de résolution des listes d’adresses de votre choix dans une `ANROrder` tableau.</span><span class="sxs-lookup"><span data-stu-id="fdc84-111">Initializes  `numANR` to the number of containers to match, and specifies the names and resolution order of the desired address lists in an  `ANROrder` array.</span></span> 
    
2. <span data-ttu-id="fdc84-112">Initialise MAPI à l’aide de la fonction **exécuter MAPIInitialize** .</span><span class="sxs-lookup"><span data-stu-id="fdc84-112">Initializes MAPI by using the **MAPIInitialize** function.</span></span> 
    
3.  <span data-ttu-id="fdc84-113">Ouvre une session sur MAPI et permet à l’utilisateur à choisir un profil.</span><span class="sxs-lookup"><span data-stu-id="fdc84-113">Logs on to MAPI and allows the user to choose a profile.</span></span> 
    
4.  <span data-ttu-id="fdc84-114">Obtient un pointeur vers le carnet d’adresses à partir de la session en cours.</span><span class="sxs-lookup"><span data-stu-id="fdc84-114">Gets a pointer to the address book from the current session.</span></span> 
    
5. <span data-ttu-id="fdc84-115">Ouvre le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="fdc84-115">Opens the Address Book.</span></span>
    
6. <span data-ttu-id="fdc84-116">Ouvre le conteneur de la racine du carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="fdc84-116">Opens the container for the root Address Book.</span></span>
    
7. <span data-ttu-id="fdc84-117">Ouvre la table de hiérarchie du conteneur de carnet d’adresses racine.</span><span class="sxs-lookup"><span data-stu-id="fdc84-117">Opens the hierarchy table of the root address book container.</span></span>
    
8. <span data-ttu-id="fdc84-118">Obtient la liste d’adresses conteneurs du carnet de dans la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="fdc84-118">Gets the list of address book containers in the hierarchy.</span></span>
    
9. <span data-ttu-id="fdc84-119">Recherche les ID d’entrée des listes d’adresses de votre choix en comparant les noms des listes d’adresses de votre choix dans `ANROrder` pour les noms dans la hiérarchie de carnets d’adresses existants.</span><span class="sxs-lookup"><span data-stu-id="fdc84-119">Looks for the entry IDs of the desired address lists by comparing the names of the desired address lists in  `ANROrder` to the existing names in the address book hierarchy.</span></span> 
    
10. <span data-ttu-id="fdc84-120">Définit l’identificateur d’entrée appropriée dans le tableau **SRowSet** , `pNewRows`.</span><span class="sxs-lookup"><span data-stu-id="fdc84-120">Sets the appropriate entry IDs to the **SRowSet** array,  `pNewRows`.</span></span>
    
11. <span data-ttu-id="fdc84-121">Appelle et transmet `pNewRows` en tant que paramètre *lpSearchPath* pour **IAddrBook::SetSearchPath** pour définir le chemin de recherche.</span><span class="sxs-lookup"><span data-stu-id="fdc84-121">Calls and passes  `pNewRows` as the  *lpSearchPath*  parameter to **IAddrBook::SetSearchPath** to set the search path.</span></span> 
    
12. <span data-ttu-id="fdc84-122">Nettoie les pointeurs et les mémoires tampons internes.</span><span class="sxs-lookup"><span data-stu-id="fdc84-122">Cleans up internal buffers and pointers.</span></span>
    
13. <span data-ttu-id="fdc84-123">Ferme la session de MAPI.</span><span class="sxs-lookup"><span data-stu-id="fdc84-123">Logs off from MAPI.</span></span>
    
14. <span data-ttu-id="fdc84-124">Uninitalizes MAPI.</span><span class="sxs-lookup"><span data-stu-id="fdc84-124">Uninitalizes MAPI.</span></span>
    
<span data-ttu-id="fdc84-125">Cet exemple de code utilise des listes d’adresses qui sont disponibles dans l’installation par défaut de Microsoft Office Outlook : **Tous les Contacts**, **Tous les groupes**et les **Contacts**.</span><span class="sxs-lookup"><span data-stu-id="fdc84-125">This code sample uses address lists that are available in the default installation of Microsoft Office Outlook: **All Contacts**, **All Groups**, and **Contacts**.</span></span> <span data-ttu-id="fdc84-126">Vous devez exécuter l’exemple après que Outlook est démarré et est en cours d’exécution sur un profil initialisé.</span><span class="sxs-lookup"><span data-stu-id="fdc84-126">You must run the sample after Outlook is started and is running on an initialized profile.</span></span> <span data-ttu-id="fdc84-127">L’exemple fonctionne correctement avec les noms qui se trouvent dans une seule langue (par exemple, tous les noms sont en anglais).</span><span class="sxs-lookup"><span data-stu-id="fdc84-127">The sample works well with names that are in one language (for example, all names are in English).</span></span> <span data-ttu-id="fdc84-128">Il n’est pas conçu pour fonctionner dans les déploiements multilingues, par exemple le dossier **Contacts** localisé pour un utilisateur qui exécutent une version anglaise Outlook.</span><span class="sxs-lookup"><span data-stu-id="fdc84-128">It is not designed to work in multi-lingual deployments, for example the **Contacts** folder localized for a user running a non-English Outlook build.</span></span> 
  
```cpp
#include "stdafx.h" 
#include <mapix.h> 
#include <mapiguid.h> 
#include <mapiutil.h> 
#include <mapidefs.h> 
#include <stdio.h> 
#include <conio.h> 
 
//Number of address lists to resolve against 
const int numANR = 3; 
WCHAR *ANROrder[numANR] = {_T("All Contacts"), _T("All Groups"), _T("Contacts")}; 
UINT  numContainersFound [numANR] = {0}; 
 
// Temporary structure to allocate buffer in MAPI. This will be used as a parent buffer to free space later. 
LPVOID tempLink; 
 
// Forward declaration of helper function to copy binary data 
STDMETHODIMP CopySBinary( 
    LPSBinary psbDest, 
    const LPSBinary psbSrc, 
    LPVOID pParent); 
 
void main() 
{ 
    // MAPI address book and session variables 
    HRESULT       hRes = S_OK;            // Result code returned from MAPI calls. 
    LPMAPISESSION lpSession = NULL;   // Pointer to MAPI session. 
    LPADRBOOK     lpAddrBook = NULL;  // Pointer to Address Book. 
 
    // Counters 
    ULONG         i = 0;                  // Index counter 
    ULONG         j = 0;                  // Index counter 
 
    // Used for querying hierarchy 
    ULONG                                   ulObjType = 0L;      // Object type returned by MAPI 
    LPMAPICONTAINER     pIABRoot = NULL;     // Root address book container 
    LPMAPITABLE              pHTable = NULL;      // Holds hierarchy table 
    LPSRowSet        pRows = NULL;        // Pointer to row set. Stores AB Address Lists 
 
    // Used for setting search path 
    LPSRowSet     pNewRows = NULL;        // Pointer to new row set 
    SizedSRowSet  (numANR, NewRows);      // New row set 
    SPropValue    sProps[numANR] = {0};   // Property tag structure 
 
    // Structures contaning MAPI Column Sets required for querying tables 
    enum { 
        abPR_ENTRYID, 
        abPR_DISPLAY_NAME_W, 
        abNUM_COLS}; 
 
    static SizedSPropTagArray(abNUM_COLS,abCols) = { 
        abNUM_COLS, 
        PR_ENTRYID, 
        PR_DISPLAY_NAME_W, 
    }; 
 
    // Initialize MAPI 
    if (FAILED ( hRes = MAPIInitialize(NULL))) goto Exit; 
 
    // Log on to MAPI and allow user to choose profile 
 
    // Note: This uses the current MAPI session if there is one 
    if (FAILED ( hRes = MAPILogonEx(NULL, NULL, NULL, MAPI_LOGON_UI, &lpSession))) goto Exit; 
 
    // Open the Address Book 
    if (FAILED (hRes = lpSession->OpenAddressBook(NULL, NULL, NULL, &lpAddrBook))) goto Cleanup; 
 
    // Open the Address Book Root container 
    if (FAILED (hRes = lpAddrBook -> OpenEntry ( 
        0L,  
        NULL, 
        NULL,  
        0L, 
        &ulObjType, 
        (LPUNKNOWN *) &pIABRoot ))) 
    goto Cleanup; 
 
    // Intentionally allocate 0 bytes. This is used for buffer management. 
    MAPIAllocateBuffer(0L, &tempLink);  
 
    // Make sure there is a Container object 
    // Query hierarchy for containers 
    if ( MAPI_ABCONT == ulObjType ) { 
        // - Call IMAPIContainer::GetHierarchyTable to open the Hierarchy 
        //   table of the root address book container 
        if ( FAILED ( hRes = pIABRoot -> GetHierarchyTable ( CONVENIENT_DEPTH | MAPI_UNICODE, 
            &pHTable ) ) ) 
        goto Cleanup; 
 
        // Get the list of address book containers first 
        if ( FAILED ( hRes = HrQueryAllRows (  
            pHTable, 
            (LPSPropTagArray) &abCols, 
            NULL, 
            NULL, 
            0L, 
            &pRows ) ) ) 
        goto Cleanup; 
 
        // Initialize the structures to set the search order 
        ZeroMemory(&NewRows, numANR * sizeof(SRow)); 
        pNewRows = (LPSRowSet)&NewRows; 
 
        // Set the number of rows you are going to set 
        pNewRows->cRows = numANR; 
 
        // Set the pointers to the structures 
        for (i=0; i<numANR; i++) 
            pNewRows->aRow[i].lpProps = &sProps[i]; 
 
        // Compare the list to the ones that of interest 
        for (i=0; i<pRows->cRows; i++) { 
            if (pRows->aRow[i].lpProps[abPR_DISPLAY_NAME_W].ulPropTag == PR_DISPLAY_NAME_W) { 
                LPWSTR containerName =  pRows->aRow[i].lpProps[abPR_DISPLAY_NAME_W].Value.lpszW; 
                for (j=0; j<numANR; j++) 
                    if (!wcscmp (containerName, ANROrder[j])) { 
                        // First check if a container with this name has been found already 
                        if (numContainersFound[j] == 0) { 
                            numContainersFound[j]++; 
                            pNewRows->aRow[j].cValues = 1; 
 
                            // The property being passing is PR_ENTRY_ID 
                            pNewRows->aRow[j].lpProps[0].ulPropTag = PR_ENTRYID; 
 
                            // Copy the binary data over 
                            if (FAILED (hRes = CopySBinary( 
                                &pNewRows->aRow[j].lpProps[0].Value.bin, 
                                &pRows->aRow[i].lpProps[abPR_ENTRYID].Value.bin, 
                                tempLink))) {  
                                    printf ("Fatal Error:Failed to copy entry IDs\n"); 
                                    goto Cleanup; 
                            } 
                         } 
                         // More than 1 container matched the same name 
                         else {  
                             printf ("Fatal Error: Duplicate container found, container name = %s\n", containerName); 
                             goto Cleanup; 
                         } 
                    } 
            } 
        } 
 
        // Only set the search path if all the rows have been found 
        // Check the array for any entries that were blank 
        for (i=0; i< numANR; i++) 
            if (numContainersFound [i] == 0) { 
                printf ("Fatal Error: all containers were not found\n"); 
                goto Cleanup; 
            } 
 
        // Everything is safe to set the search path now 
        if (FAILED (hRes = lpAddrBook->SetSearchPath(0, pNewRows))) {                    
            printf ("Fatal Error: failed to set the search path\n"); 
            goto Cleanup; 
        } 
    } 
 
    Cleanup: 
        MAPIFreeBuffer(tempLink); 
        UlRelease(pHTable); 
        FreeProws(pRows); 
        UlRelease (pIABRoot); 
        UlRelease(lpAddrBook); 
 
        // Log off from MAPI 
        hRes = lpSession->Logoff(NULL, NULL, 0); 
        UlRelease(lpSession); 
 
    Exit: 
        // Uninitialize MAPI 
        MAPIUninitialize(); 
} 
 
///////////////////////////////////////////////////////////// 
//    CopySBinary() 
// 
//    Parameters 
// 
//    Purpose 
//      Allocates a new SBinary and copies psbSrc into it 
// 
 
STDMETHODIMP CopySBinary( 
    LPSBinary psbDest, 
    const LPSBinary psbSrc, 
    LPVOID pParent) 
{ 
    HRESULT     hRes = S_OK; 
    psbDest->cb = psbSrc->cb; 
 
    if (psbSrc->cb) { 
        if (pParent) 
            hRes = MAPIAllocateMore( 
                 psbSrc->cb, 
                 pParent, 
                 (LPVOID*) &psbDest->lpb); 
        else 
            hRes = MAPIAllocateBuffer( 
                 psbSrc->cb, 
                 (LPVOID*) &psbDest->lpb); 
 
    if (!FAILED(hRes)) 
        CopyMemory(psbDest->lpb,psbSrc->lpb,psbSrc->cb); 
    } 
 
   return hRes; 
} 

```

## <a name="see-also"></a><span data-ttu-id="fdc84-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fdc84-129">See also</span></span>

- [<span data-ttu-id="fdc84-130">À propos de la définition de l’ordre de résolution pour les listes d’adresses dans Outlook</span><span class="sxs-lookup"><span data-stu-id="fdc84-130">About Setting the Resolution Order for Address Lists in Outlook</span></span>](about-setting-the-resolution-order-for-address-lists-in-outlook.md)

