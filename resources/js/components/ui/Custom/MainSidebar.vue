<script setup lang="ts">
import {
  Sidebar,
  SidebarContent,
  SidebarFooter,
  SidebarGroup,
  SidebarHeader,
  SidebarGroupLabel,
  SidebarGroupContent,
  SidebarMenu,
  SidebarMenuItem,
  SidebarMenuButton
} from '@/components/ui/sidebar'
import { Database, LayoutDashboard, SquareChartGantt } from 'lucide-vue-next';
</script>

<template>
  <Sidebar>
    <SidebarHeader />
    <SidebarContent>
        <SidebarGroup>
            <SidebarGroupLabel>Default</SidebarGroupLabel>
            <SidebarGroupContent>
            <SidebarMenu>
                <SidebarMenuItem>
                    <SidebarMenuButton asChild>
                        <a href="#">
                            <component :is="LayoutDashboard" />
                            <span>Dashboard</span>
                        </a>
                    </SidebarMenuButton>
                </SidebarMenuItem>
                <SidebarMenuItem>
                    <SidebarMenuButton asChild>
                        <a href="#">
                            <component :is="SquareChartGantt" />
                            <span>Categories</span>
                        </a>
                    </SidebarMenuButton>
                </SidebarMenuItem>
                <SidebarMenuItem>
                    <SidebarMenuButton asChild>
                        <a href="#">
                            <component :is="Database" />
                            <span>Datamanager</span>
                        </a>
                    </SidebarMenuButton>
                </SidebarMenuItem>
            </SidebarMenu>
            </SidebarGroupContent>
        </SidebarGroup>
    </SidebarContent>
    <SidebarFooter />
  </Sidebar>
</template>
