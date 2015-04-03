## CMake List Files for EnergyPlus v. 7.2

## CMake Version
cmake_minimum_required(VERSION 2.8)

## Project Name
project(EnergyPlus)

## Use FORTRAN
enable_language(Fortran)

## Release compiler options
set (CMAKE_Fortran_FLAGS_RELEASE "-O -cpp -ffree-line-length-none -fimplicit-none -static-libgcc -static-libstdc++ -static-libgfortran")

## Debug compiler options
set (CMAKE_Fortran_FLAGS_DEBUG "-g -cpp -ffree-line-length-none -fimplicit-none")

## Set directory for FORTRAN modules
set (CMAKE_Fortran_MODULE_DIRECTORY "${EnergyPlus_BINARY_DIR}/modules")

## Build Executable
add_executable(EnergyPlus/EnergyPlus 
	       AirflowNetworkBalanceManager.f90 
	       AirflowNetworkSolver.f90	       
	       BaseboardRadiator.f90 
	       BaseboardRadiatorElectric.f90
	       BaseboardRadiatorSteam.f90 
	       BaseboardRadiatorWater.f90 
	       BranchInputManager.f90 
	       BranchNodeConnections.f90
	       ConductionTransferFunctionCalc.f90 
	       CoolTower.f90
	       CostEstimateManager.f90 
	       CurveManager.f90 
	       DataAirflowNetwork.f90
	       DataAirLoop.f90 
	       DataAirSystems.f90 
	       DataBranchAirLoopPlant.f90
	       DataBSDFWindow.f90
	       DataBranchNodeConnections.f90 
	       DataComplexFenestration.f90
	       DataContaminantBalance.f90
	       DataConvergParams.f90 
	       DataConversions.f90 
	       DataCostEstimate.f90 
	       DataDaylighting.f90 
	       DataDaylightingDevices.f90 
	       Datadefineequip.f90 
	       DataDElight.f90 
	       DataEnvironment.f90
	       DataEquivalentLayerWindow.f90 
	       DataErrorTracking.f90
	       DataGenerators.f90 
	       DataGlobalConstants.f90 
	       DataGlobals.f90
	       DataHeatBalance.f90 
	       DataHeatBalFanSys.f90 
	       DataHeatBalSurface.f90
	       DataHVACControllers.f90 
	       DataHVACGlobals.f90 
	       DataInterfaces.f90
	       DataIPShortCuts.f90 
	       DataLoopNode.f90 
	       DataMoistureBalance.f90
	       DataMoistureBalanceEMPD.f90 
	       DataOutputs.f90 
	       DataPhotovoltaics.f90 
	       DataPlant.f90 
	       DataPlantPipingSystems.f90 
	       DataPrecisionGlobals.f90
	       DataReportingFlags.f90 
	       DataRoomAir.f90 
	       DataRootFinder.f90
	       DataRuntimeLanguage.f90 
	       DataShadowingCombinations.f90 
	       DataSizing.f90
	       DataStringGlobals.f90 
	       DataSurfaceColors.f90 
	       DataSurfaceLists.f90
	       DataSurfaces.f90 
	       DataSystemVariables.f90 
	       DataTimings.f90 
	       DataUCSDSharedData.f90 
	       DataVectorTypes.f90
	       DataViewFactorInformation.f90 
	       DataWater.f90 
	       DataZoneControls.f90
	       DataZoneEnergyDemands.f90 
	       DataZoneEquipment.f90
	       DaylightingDevices.f90
	       DaylightingManager.f90
	       DElightManagerF_NO.f90
	       DemandManager.f90
	       DesiccantDehumidifiers.f90
	       DirectAir.f90
	       DisplayRoutines.f90
	       DXCoil.f90
	       EarthTube.f90
	       EconomicLifeCycleCost.f90
	       EconomicTariff.f90 
	       EcoRoof.f90
	       ElectricPowerGenerators.f90 
	       ElectricPowerManager.f90 
	       EMSManager.f90
	       EnergyPlus.f90 
	       ExteriorEnergyUseManager.f90 
	       ExternalInterface_NO.f90
	       FanCoilUnits.f90 
	       FaultsManager.f90
	       FluidProperties.f90 
	       General.f90 
	       GeneralRoutines.f90
	       GlobalNames.f90 
	       HeatBalanceAirManager.f90
	       HeatBalanceConvectionCoeffs.f90 
	       HeatBalanceHAMTManager.f90
	       HeatBalanceInternalHeatGains.f90
	       HeatBalanceIntRadExchange.f90
	       HeatBalanceManager.f90 
	       HeatBalanceMovableInsulation.f90
	       HeatBalanceSurfaceManager.f90 
	       HeatBalFiniteDifferenceManager.f90
	       HeatRecovery.f90 
	       Humidifiers.f90 
	       HVACControllers.f90
	       HVACCooledBeam.f90 
	       HVACDualDuctSystem.f90 
	       HVACDuct.f90
	       HVACDXSystem.f90 
	       HVACEvapComponent.f90 
	       HVACFanComponent.f90
	       HVACFurnace.f90 
	       HVACHeatingCoils.f90 
	       HVACHXAssistedCoolingCoil.f90
	       HVACInterfaceManager.f90 
	       HVACManager.f90 
	       HVACMixerComponent.f90
	       HVACMultiSpeedHeatPump.f90 
	       HVACSingleDuctInduc.f90
	       HVACSingleDuctSystem.f90 
	       HVACSplitterComponent.f90
	       HVACStandAloneERV.f90 
	       HVACSteamCoilComponent.f90
	       HVACTranspiredCollector.f90 
	       HVACUnitaryBypassVAV.f90
	       HVACUnitarySystem.f90
	       HVACVariableRefrigerantFlow.f90 
	       HVACWaterCoilComponent.f90
	       HVACWatertoAir.f90 
	       HVACWatertoAirMultiSpeedHP.f90 
	       InputProcessor.f90
	       MatrixDataManager.f90
	       MixedAir.f90
	       MoistureBalanceEMPDManager.f90
	       NodeInputManager.f90
	       NonZoneEquipmentManager.f90 
	       OutAirNodeManager.f90 
	       OutdoorAirUnit.f90
	       OutputProcessor.f90 
	       OutputReportPredefined.f90 
	       OutputReports.f90
	       OutputReportTabular.f90 
	       PackagedTerminalHeatPump.f90
	       PackagedThermalStorageCoil.f90
	       Photovoltaics.f90 
	       PhotovoltaicThermalCollectors.f90
	       PlantAbsorptionChillers.f90 
	       PlantBoilers.f90 
	       PlantBoilersSteam.f90
	       PlantCentralGSHP.f90
	       PlantChillers.f90 
	       PlantCondLoopOperation.f90 
	       PlantCondLoopTowers.f90
	       PlantEIRChillers.f90 
	       PlantEvapFluidCoolers.f90
	       PlantExhaustAbsorptionChiller.f90 
	       PlantFluidCoolers.f90
	       PlantGasAbsorptionChiller.f90
	       PlantGroundHeatExchangers.f90 
	       PlantHeatExchanger.f90
	       PlantIceThermalStorage.f90 
	       PlantLoadProfile.f90
	       PlantLoopEquipment.f90 
	       PlantLoopSolver.f90 
	       PlantManager.f90
	       PlantOutsideEnergySources.f90 
	       PlantPipeHeatTransfer.f90
	       PlantPipes.f90 
	       PlantPipingSystemManager.f90
	       PlantPondGroundHeatExchanger.f90
	       PlantPressureSystem.f90
	       PlantPumps.f90 
	       PlantSolarCollectors.f90
	       PlantSurfaceGroundHeatExchanger.f90
	       PlantUtilities.f90
	       PlantValves.f90
	       PlantWaterSources.f90
	       PlantWaterThermalTank.f90
	       PlantWatertoWaterGSHP.f90
	       PlantWaterUse.f90 
	       PollutionAnalysisModule.f90
	       PoweredInductionUnits.f90 
	       PsychRoutines.f90 
	       Purchasedairmanager.f90
	       RadiantSystemHighTemp.f90 
	       RadiantSystemLowTemp.f90
	       RefrigeratedCase.f90 
	       ReportSizingManager.f90 
	       ReturnAirPath.f90
	       RoomAirManager.f90 
	       RoomAirModelCrossVent.f90
	       RoomAirModelDisplacementVent.f90 
	       RoomAirModelMundt.f90
	       RoomAirModelUFAD.f90 
	       RoomAirModelUserTempPattern.f90 
	       RootFinder.f90
	       RuntimeLanguageProcessor.f90 
	       ScheduleManager.f90 
	       SetPointManager.f90
	       SimAirServingZones.f90 
	       SimulationManager.f90 
	       SizingManager.f90
	       SolarReflectionManager.f90 
	       SolarShading.f90
	       SortAndStringUtilities.f90 
	       SQLiteFortranRoutines_NO.f90
	       StandardRatings.f90 
	       SurfaceGeometry.f90 
	       SystemAvailabilityManager.f90 
	       SystemReports.f90 
	       TarcogComplexFenestration.f90
	       ThermalChimney.f90 
	       ThermalComfort.f90
	       UnitHeater.f90 
	       UnitVentilator.f90 
	       UserDefinedComponents.f90
	       UtilityRoutines.f90 
	       VectorUtilities.f90 
	       VentilatedSlab.f90
	       WaterManager.f90 
	       WeatherManager.f90 
	       WindowAC.f90 
	       WindowComplexManager.f90
	       WindowEquivalentLayer.f90
	       WindowManager.f90
	       WindTurbine.f90 
	       Zoneairloopequipmentmanager.f90
	       ZoneContaminantPredictorCorrector.f90 
	       ZoneDehumidifier.f90
	       Zoneequipmentmanager.f90 
	       ZonePlenumComponent.f90 
	       ZoneTempPredictorCorrector.f90)
	       
## Set extension
set_target_properties(EnergyPlus/EnergyPlus PROPERTIES SUFFIX ".exe")

## Move IDD file to build directory for testing
add_custom_target(CopyIDD ALL
				   COMMAND ${CMAKE_COMMAND} -E make_directory EnergyPlus
				   COMMAND ${CMAKE_COMMAND} -E copy_if_different
				   ../../resource/Energy+.idd 
				   EnergyPlus/)